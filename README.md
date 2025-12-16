# Automating Creative AI for Accessible Image Editing
This project is a collaboration with Yum Me Print to let users edit their images using simple, natural language prompts. A common problem with AI models is that creating good prompts takes time and expertise, and poor prompts can result in low-quality image edits. This project aims to reduce manual work for users by allowing them to easily select and customize features using Nano Banana generative models for image editing. The system also verifies whether the generated images match with prompt.<br />

This project can dividend into 4 part:<br />

Input Image Analysis <br />
Prompt Generation <br />
Image Editing by using Nano banana <br />
Result Verification <br />

| Model Pipeline     | Algorithms                                 | Applications                                                                                                     |
|--------------------|--------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| Detection          | YOLOv8 / MTCNN / RetinaFace                | Identify input type (portrait, object, scenery)<br>Face localization before processing                           |
| Embedding          | ArcFace / FaceNet / InsightFace–buffalo_l  | Compare similarity before/after edit<br>Identity preservation<br>Prevent mis-generation (wrong face, wrong person)|
| Vision Language    | BLIP                                       | Auto-generate BLG editing prompt<br>Extract subjects, colors, objects                                            |
| Image Generation   | Nano-Banana                                | Apply background/clothing/style changes<br>Produce final edited image                                            |
| Verification       | FaceNet / MTCNN / YOLOv8                   | Face similarity & age consistency check<br>Detect identity distortion<br>Background/object changes               |
| Classification     | ResNet-18 / CNN Classifier                 | ID-photo recognition<br>Dataset labeling<br>Assist quality control                                               |
