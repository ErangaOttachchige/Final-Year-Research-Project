# Final-Year-Research-Project
Robust detection and species classification of wildlife in low-light camera-trap images, with an “empty-image” verifier and a lightweight pipeline (image enhancement → detection → species classifier) suitable for a mobile prototype.


For the final pipeline, Stage 1 must come before Stage 2:

✅ Recommended order:

Stage 1 = detector/filter: empty vs animal vs car
→ then if predicted “animal” →
Stage 2 = species classification (12 classes)

So now that Stage 2 is trained, the next correct step is:

✅ Train Stage 1 (3-class classifier) using cct20_stage1_imagelevel.csv

Because your real pipeline is:
Input image → Stage 1 (empty/animal/car) → if animal → Stage 2 species
