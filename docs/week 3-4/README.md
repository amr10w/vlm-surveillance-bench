- Step 1 Collecting the dataset ⇒ explore the models capabilities
    
    45 frame, 30 clips
    
    | **Event type** | Fight, hitting, fire, crowd congestion, abandoned object, panic attack |
    | --- | --- |
    | **Quality** | Low, high |
    | **Lighting** | Night (vs. day) |
    | **Camera angle** | Angle variety (e.g., overhead, eye-level, oblique, far/near) |
    | **Length** | Still undefined (short / medium / long) |
    |  |  |
- Step 2 Setting up the environment —
    
    make GitHub
    
- Step 3 research in the metrices then defining them
    - latency, hit rate@k, MRR, recall@k.
    - **CIDEr, SPICE** (+ BLEU-4, METEOR, ROUGE-L in the appendix)
    - **BERTScore** or embedding similarity
    - **LLM-judge:** correctness, completeness, **hallucination → An API model is the most reliable choice here**
    - Event F1, counting error, false-alarm rate
    - Latency, VRAM, tokens/sec
    - Relative score = candidate's score ÷ reference's score, as a percentage.
    - **Human ceiling** for all of the above
- Step 4  choosing the models [ 1→4 small, 7→ 12 medium, api]
    
    
- Step 5 experiments // evaluation
    - zero-shot baseline on all models.
    - prompt engineering variants, plus the IP experiment if you've clarified what it is.
    - perception vs. without perception, and counting, on the top model(s).
    - quantization 4-bit vs. 16-bit on the top model, then consolidate the full results table (the "evaluation" step).
- Step 6 research is finetuning reliable
    
    
- Step 7 Analysis and outputs
    - Ability matrix: models vs. capabilities.
    - Risk analysis: failure modes, how often, how severe.
- Step 8 Building the small app
