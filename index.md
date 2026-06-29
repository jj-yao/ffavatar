---
layout: project_page
permalink: /

title: "FFAvatar: Feed-Forward 4D Head Avatar Reconstruction from Sparse Portrait Images"

authors:
    Jianjiang Yao, Ke Xian, Renxiang Dai, Caiming Qiu 
affiliations:
    Huazhong University of Science and Technology
paper: "coming-soon"
video: "coming-soon"
code: "coming-soon"
# data: https://huggingface.co/docs/datasets
---

<!-- Abstract -->
<div class="columns is-centered has-text-centered">
    <div class="column is-four-fifths">
        <h2 style="margin-bottom: 0.8rem;">Abstract</h2>
        <div class="content has-text-justified">
            <p>
We present FFAvatar, a Transformer-based 3D Gaussian framework for fast construction of high-quality and animatable 4D head avatars from one or more reference portrait images. Unlike existing feed-forward approaches that require a fixed number of input views, FFAvatar supports <em>incremental reconstruction</em>, progressively refining the avatar representation as additional reference images become available.
            </p>
            <p>
At the core of our method is an alternating attention mechanism that disentangles identity appearance from expression and viewpoint variations, enabling the reconstruction of a canonical 3D appearance that remains consistent across poses and facial expressions. To balance visual fidelity and computational efficiency, we introduce a sparse-to-dense learning paradigm. Coarse appearance features are first learned using sparse primitives anchored to the FLAME vertex level and are subsequently densified in the UV domain to capture fine-grained geometric and texture details.
            </p>
            <p>
We further propose a plug-and-play motion refinement module that enables subject-specific dynamic personalization by modeling residual motion beyond parametric deformation. Extensive experiments demonstrate that FFAvatar efficiently produces high-fidelity and controllable 4D head avatars, achieving superior flexibility, driving efficiency, and identity-consistent rendering across diverse expressions and viewpoints.
            </p>
        </div>
    </div>
</div>

<hr style="max-width: 80%; margin: 2rem auto; border: none; border-top: 1px solid #e0e0e0;">

<!-- Method -->
<div class="columns is-centered has-text-centered">
    <div class="column">
        <h2 style="margin-bottom: 1.2rem;">Method</h2>
        <figure style="margin: 0 auto; display: inline-block;">
            <img src="/static/image/FFAvatar.svg" alt="FFAvatar Overview" style="max-width: 100%;">
            <figcaption style="margin-top: 0.8rem; font-size: 0.9em; color: #555; text-align: justify; line-height: 1.6; max-width: 900px; margin-left: auto; margin-right: auto;">
                <strong>Figure 1: Overview of FFAvatar.</strong>
                <strong style="color: #333;">Canonical field modeling.</strong> Visual features extracted by DINOv3 are concatenated with camera pose and expression encodings. An alternating attention mechanism performs intra- and inter-image matching to infer a consistent global appearance representation across all inputs. This representation is then aligned with the FLAME template through the proposed Sparse-to-Dense Cross-modal Alignment Module, producing an expression- and viewpoint-invariant static 3D appearance.
                <strong style="color: #333;">Deformable field modeling.</strong> Facial motions are driven by the FLAME model using standard linear blend skinning (LBS) and corrective blendshapes, and further refined by the proposed Motion-Aware Refinement Module to capture fine-grained, identity-dependent dynamic details.
            </figcaption>
        </figure>
    </div>
</div>

<hr style="max-width: 80%; margin: 2rem auto; border: none; border-top: 1px solid #e0e0e0;">

<!-- Video -->
<div class="columns is-centered has-text-centered">
    <div class="column">
        <h2 style="margin-bottom: 1.2rem;">Video</h2>
        <div style="max-width: 960px; margin: 0 auto;">
            <video src="static/image/Video_h264.mp4" controls width="100%" style="border-radius: 8px; box-shadow: 0 2px 12px rgba(0,0,0,0.1);"></video>
        </div>
    </div>
</div>
