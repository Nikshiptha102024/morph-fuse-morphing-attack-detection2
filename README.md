# MORPH-FUSE: SelfMAD++ and Vision Transformer fusion for morphing attack detection

Summer internship project, NIT Calicut (guide: Dr. Anil Pinapati).

## What this is
Reproduction of SelfMAD++ (Ivanovska et al., 2026), an implementation of the
ViT-based S-MAD detector (Zhang et al., 2025), and a score-level fusion of the two.
Evaluated on the open FRLL-Morphs dataset (AMSL, FaceMorpher, OpenCV, StyleGAN, WebMorph).

## Results (EER %)
<img width="482" height="610" alt="image" src="https://github.com/user-attachments/assets/2f9cba26-7efd-416e-ab5e-e6531a627add" />


## What is mine and what is not
- SelfMAD++: authors' released checkpoint, evaluated by me (not retrained)
- ViT-based detector: my implementation (MTCNN crop, ViT-L features, linear SVM)
- Fusion: average of the two scores
- Limitation: bona fide images were reused in SVM training and testing, so the
  ViT and fused numbers are optimistic

## How to run
1. Open the notebooks in Google Colab (T4 GPU).
2. Get SelfMAD++ code and checkpoint from https://github.com/LeonTodorov/SelfMADpp
3. Get FRLL-Morphs (Zenodo) and the FRLL faces (Figshare)

## References
[1] M. Ivanovska, L. Todorov, P. Peer, and V. ˇ Struc, “SelfMAD++: Self-Supervised Foun
dation Model with Local Feature Enhancement for Generalized Morphing Attack Detec
tion,” Information Fusion, vol. 127, Art. no. 103921, Mar. 2026.
[2] H. Zhang, R. Ramachandra, K. Raja, and C. Busch, “Generalized Single-Image-Based
Morphing Attack Detection Using Deep Representations from Vision Transformer,”
arXiv:2501.09817, 2025.
