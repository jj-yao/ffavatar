---
layout: project_page
permalink: /

title: "FFAvatar: Feed-Forward 4D Head Avatar Reconstruction from General Portrait Images"

authors:
    Jianjiang Yao, Ke Xian, Renxiang Dai, Caiming Qiu 
affiliations:
    Huazhong University of Science and Technology
paper: "coming-soon"
video: "coming-soon"
code: "coming-soon"
data: "coming-soon"
# data: https://huggingface.co/docs/datasets
---

<!-- Using HTML to center the abstract -->
<div class="columns is-centered has-text-centered">
    <div class="column is-four-fifths">
        <h2>Abstract</h2>
        <div class="content has-text-justified">
We present FFAvatar, a Transformer-based 3D Gaussian framework for fast construction of high-quality and animatable 4D head avatars from unconstrained image collections. Unlike existing feed-forward approaches that require a fixed number of input views, FFAvatar supports incremental reconstruction, progressively refining the avatar representation as additional reference images become available.
At the core of our method is an alternating attention mechanism that disentangles identity appearance from expression and viewpoint variations, enabling the reconstruction of a canonical 3D appearance that remains consistent across poses and facial expressions. To balance visual fidelity and computational efficiency, we introduce a sparse-to-dense learning paradigm. Coarse appearance features are first learned using sparse primitives anchored to the FLAME vertex level and are subsequently densified in the UV domain to capture fine-grained geometric and texture details.
We further propose a plug-and-play motion refinement module that enables subject-specific dynamic personalization by modeling residual motion beyond parametric deformation. Extensive experiments demonstrate that FFAvatar efficiently produces high-fidelity and controllable 4D head avatars, achieving superior flexibility, driving efficiency, and identity-consistent rendering across diverse expressions and viewpoints.
        </div>
    </div>
</div>



## Method

![FFAvatar Overview](/static/image/FFAvatar.svg)

*Figure 1: Overview of FFAvatar. **Canonical field modeling.** Visual features extracted by DINOv3 are concatenated with camera pose and expression encodings. An alternating attention mechanism performs intra- and inter-image matching to infer a consistent global appearance representation across all inputs. This representation is then aligned with the FLAME template through the proposed Sparse-to-Dense Cross-modal Alignment Module, producing an expression- and viewpoint-invariant static 3D appearance. **Deformable field modeling.** Facial motions are driven by the FLAME model using standard linear blend skinning (LBS) and corrective blendshapes, and further refined by the proposed Motion-Aware Refinement Module to capture fine-grained, identity-dependent dynamic details.*

## Video
<video src="static/image/ECCV2026_7586_h264.mp4" controls width="1280"></video>
