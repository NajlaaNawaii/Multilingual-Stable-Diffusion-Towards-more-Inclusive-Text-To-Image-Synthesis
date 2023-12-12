# Multilingual-Stable-Diffusion-Towards-more-Inclusive-Text-To-Image-Synthesis
### Stable Diffusion Model that speaks 40 languages! - BSc Thesis

## Overview

This repository presents a specialized variant of the Stable Diffusion model designed for multilingual text-to-image synthesis. In response to the observed underperformance of existing models on languages beyond English, this project introduces the Multilingual Stable Diffusion, providing a more inclusive solution for diverse linguistic contexts.

## Why Multilingual Stable Diffusion?

Stable Diffusion, while powerful, faces challenges when applied to languages other than English. CLIP and Stable Diffusion models often underperform when tested on non-English data. To address this limitation, we introduce a multilingual variant that leverages the strengths of Stable Diffusion while accommodating up to 40 languages. Our aim is to enhance the accessibility of text-to-image diffusion models, promoting cultural understanding and inclusivity.

## Multilingual Features

The Multilingual Stable Diffusion is tailored to:

1.   Generate Culturally Relevant Images  : Our model is trained to produce images that align with the cultural nuances of various languages.

2.   Support Multiple Languages  : With a focus on inclusivity, this variant enables text-to-image generation in up to 40 languages, promoting a more diverse range of creative outputs.

3.   Adapter Layer for Alignment  : We introduce an adapter layer to bridge the gap between multilingual-CLIP and the original CLIP, ensuring effective communication between text embeddings and the decoder.

## Training Process

The training of Multilingual Stable Diffusion involves a two-stage process:

1.   Integration of Multilingual-CLIP  : We substitute the original CLIP text-encoder with the multilingual version and directly pass text embeddings from multilingual-CLIP to the decoder.

2.   Adapter Layer Training  : An adapter module is introduced and exclusively trained on English captions to align multilingual-CLIP's output with the original CLIP's embedding space. This ensures effective cross-linguistic text-to-image generation.

## Dataset Used

The model is trained on a diverse dataset, including English captions from the LAION-2B-en dataset. This dataset encompasses approximately 12,500 English captions, serving as a foundation for training the adapter module.

## Performance Evaluation

The effectiveness of Multilingual Stable Diffusion is demonstrated through qualitative analysis against baseline models, including the original Stable Diffusion and a variant without the adapter layer ("No Adapter"). The model excels in generating culturally relevant images, addressing the limitations observed in the original Stable Diffusion.
<img src="./Images/side-by-side comparison.png" alt="img">
Figure 1: Samples of generations from multilingual prompts from Stable Diffusion, No Adapter
and Ours, left to right.


## Results

Evaluation results, with a focus on the Arabic text caption subset, showcase significant improvements in performance:

  Table 1: Arabic Language Evaluation - FID and CLIP Scores Comparison  

| Model                      | FID Score | CLIP Score |
| ---------------------------|-----------|------------|
| Original Stable Diffusion  | 132.23    | 8.07       |
| Multilingual Stable Diffusion| 50.99   | 18.2       |

These results highlight a 61.47% FID score improvement and a 125% CLIP score improvement, affirming the efficacy of the multilingual approach.

## Conclusion

This project introduces Multilingual Stable Diffusion as a step towards a more inclusive text-to-image synthesis experience. By leveraging multilingual-CLIP and training an adapter layer, we enhance Stable Diffusion's ability to handle non-English text, making strides toward bridging the gap between linguistic diversity and AI-generated visuals. 



