# okvqa-privacy-attribute

This json file (`annotations.json`) contains privacy attribute annotations of the two subsets ('People and Everyday life' and 'Sports and Recreation) in OK-VQA val set used in Boundary Probing for Input Privacy Protection When Using LMM Services (ICCV2025). The corresponding images can be downloaded from OK-VQA dataset (https://okvqa.allenai.org).

Following previous works, the annotated privacy attributes are gender ("a4_gender"), complete face ("a9_face_complete"), partial face ("a10_face_partial"), skin color ("a17_color"), semi-nudity ("a12_semi_nudity"), personal relationship ("a64_rel_personal"), and social relationship ("a65_rel_social").

### Annotation information
Each annotation entry corresponds to a specific image and is labeled with its privacy attributes, containing:

`id` (int): A unique identifier for the image within the annotation set.

`image` (str): image name of the corresponding image file.

`choice` (str or dict, optional): The annotated attribute(s), either as:
- A single string label.
- A dictionary with a choices key listing multiple labels.
- Omitted as the image does not contain these privacy attributes.

Example:
```
{
    "image": "COCO_val2014_000000010825.jpg",
    "id": 33,
    "choice": {
        "choices": [
            "a17_color",
            "a4_gender",
            "a10_face_partial"
        ]
    }
}
```
This image is annotated with privacy attributes 'skin color', 'gender', and 'partial face'.



[1] Orekondy, Tribhuvanesh, Bernt Schiele, and Mario Fritz. "Towards a visual privacy advisor: Understanding and predicting privacy risks in images." Proceedings of the IEEE international conference on computer vision. 2017.

[2] Dave, Ishan Rajendrakumar, Chen Chen, and Mubarak Shah. "Spact: Self-supervised privacy preservation for action recognition." Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition. 2022.
