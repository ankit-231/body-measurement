# Body Measurement

# Logs

## Day 1

Due to my other works, I will explore the models, maybe spin up a minimal example. I currently have 8.71 GB space on my laptop. It's a 16 GB laptop. I'll see if the pre-trained models function in this environment. If not, I'll search for a smaller model.

I thought of using [mediapipe](https://github.com/google-ai-edge/mediapipe) which I have an experience on from another project: [workout tracker](https://github.com/ankit-231/swotaha-be), but I used it specifically to track joints and angle between them to create the workout tracking logic. And a little bit of research (using LLMs of course shows that it can be pretty limiting).

- For waist: there's no waist landmark. People usually fake it by taking the horizontal distance between the hip landmarks, which is a skeletal measurement.
- Without a reference (known height, a checkerboard, a card of known size, or a calibrated camera/focal length), you can get ratios between body parts but not real cm/inches.
- Waist/chest circumference requires knowing the cross-sectional shape of the torso (roughly elliptical), which needs either a second orthogonal view (front + side) or a strong shape prior.
- Loose clothing hides the actual body contour under the fabric silhouette.

So (also, as suggested by the assessment docx) I'll use SMPLer-X or equivalent pre-trained models

### Need to move to google colab

Just found out my laptop ain't gonna be able to support the model. Will use google colab. Hopefully I will find a way to create a temporary minimal FastAPI endpoint and expose it to ngrok for a public demo later on. We'll find out as we explore.

I'll use the pre-built notebook: https://colab.research.google.com/github/camenduru/SMPLer-X-colab/blob/main/SMPLer_X_colab.ipynb

Here's my fork (deprecated, see Day 4): https://colab.research.google.com/drive/1hsJsVNHT2KG1E1H8FB2ZSEA4KbrZpe4f?usp=sharing

### Day 2

Could not do it, because I was busy for in-person technical round for another company and was completely burnt out. See: https://github.com/ankit-231/event-mgmt-assessment

### Day 3

Will do it.

### Day 4
I'm setting up SMPLest-X in google colab.

New Link: https://drive.google.com/file/d/1eOGZnm40s2VbhLm05GLtRR3giGYUxdVg/view?usp=sharing


#### 04:45 PM
Finally setup colab to generate pictures with mesh around it.
<img width="1920" height="999" alt="image" src="https://github.com/user-attachments/assets/d6b6b313-6029-4695-9d1e-de91eb48ab43" />

Woman Before:
<img width="2000" height="3000" alt="person_woman" src="https://github.com/user-attachments/assets/c97f1818-0cfa-405b-8e0d-06fac0de9a12" />


Woman Result:
<img width="2000" height="3000" alt="result_person_woman" src="https://github.com/user-attachments/assets/b96f8f02-64fd-4425-9ae2-3c12a37cf75f" />

Man Before:
<img width="3210" height="4815" alt="person_man_1" src="https://github.com/user-attachments/assets/42f23ca1-8016-4f7c-b4ea-c355854526d9" />

Man Result:
<img width="3210" height="4815" alt="result_person_man_1" src="https://github.com/user-attachments/assets/94ce4429-d5f0-409b-af95-7281af932501" />

