# HHA504_assignment_ai

## Work with Pre-trained Speech Models ##
### GCP Speech-to-Text ###

I was able to easily navigate to Verex AI and spent some time checking all the model options. 

<img width="932" alt="image" src="https://github.com/user-attachments/assets/ebef6943-3569-4f4e-8f54-48081137b273">

I decided to go with Chirp 2, a speech-to-text module that would cost $0.016/min.

<img width="731" alt="image" src="https://github.com/user-attachments/assets/a7b4c04c-fe24-4a93-a269-0a9f468117e5">
<img width="488" alt="image" src="https://github.com/user-attachments/assets/6328696f-c4c0-4ed1-ab2f-b604f663bfc6">


*(I realized Later that I could just go in the side panel under the Vertex AI studio and click on 'speech' and it would automatically bring me there)* 

<img width="941" alt="image" src="https://github.com/user-attachments/assets/dbf06397-0ff7-4d2a-8b5f-7c7f25f43ce3">


I found an audio smaple from Kaggle and uploaded the file. 

<img width="668" alt="image" src="https://github.com/user-attachments/assets/1f10908e-91dd-40eb-bba3-4cc511573728">

After hitting the submit button, the audio was transcribed. There were some errors, though nothing too drastic. I would say it makes the same amount of errros as my phone when I'm trying to use the speech-to-text option on iMessage.  

<img width="852" alt="image" src="https://github.com/user-attachments/assets/4f6375b7-3620-41cd-bf9c-b900377d1bc0">

This model also had a text-to-speech option and it worked just fine. My only critique is that the 'spanish voice' option should have a note that it doesn't translate the text written in English, it just pronounces the English word with Spanish anunciation. 

<img width="877" alt="image" src="https://github.com/user-attachments/assets/35c31f14-59f3-410d-b82f-a9395019ef70">


## Work with Pre-trained Vision Models ##
### GCP Vision API ###

Unlike the Speech model, the vision model was restricted and required requesting access. 

<img width="925" alt="image" src="https://github.com/user-attachments/assets/45b03ec7-9515-4671-8c2e-9226859dc661">

I clicked on the 'Prompt Gallery' under the Vertex AI Studio and found an 'extract text from image' task. 

<img width="932" alt="image" src="https://github.com/user-attachments/assets/1ae01a16-b11e-47e5-b995-e37c68690cbd">

The preset image was a handwritten note and the prompt was to 'read the text in this image'. 

<img width="767" alt="image" src="https://github.com/user-attachments/assets/2392d079-8c51-4045-8977-b66780906e4e">

After clicking the submit button, a transcription of the text in the image was written. 
<img width="744" alt="image" src="https://github.com/user-attachments/assets/ce613991-1e48-460b-8ed8-4981a05a7057">

I uploaded a more text heavy image and decided to see what response would be generated. 

<img width="843" alt="image" src="https://github.com/user-attachments/assets/33565ddd-ebdd-494c-b608-94e6be83daf5">

Instead of transcribing word for word like the previous image, the response box provided a breakdown of what text was in the image in a summary format. 

![image](https://github.com/user-attachments/assets/30a11e91-91a5-4f49-ab32-d40a9b3b3751)

<img width="491" alt="image" src="https://github.com/user-attachments/assets/4b986005-1198-438b-be53-f1e6ed703848">

Overall, the prompt gallery seems like a much easier and quicker way of performing a task. It has the same user-firendly format as ChatGPT, where you you enter a prompt and it generates a response. And like ChatGPT, it will also provide suggestions on new prompts. 

<img width="920" alt="image" src="https://github.com/user-attachments/assets/da4c9bc3-48d7-48df-89b3-4f3d51b8beca">

Before finding the 'Prompt Gallery', I had actually looked for a Vision API model in the 'Model Garden'. 

There were 88 different models to choose from, broken down into three levels: 
  1) Foundation models: Pre-trained multi-task models that can be further tuned or customized for specific tasks.
  2) Fine-tunable models: Models that data scientists can further fine-tune through a custom notebook or pipeline.
  3) Task-specific solutions: Most of these pre-built models are ready to use off the shelf, and many can be customized using your own data.

The 'Task=specific solutions' had 20 different models, including the text detector and face detecor from the Vision API model. 

<img width="845" alt="image" src="https://github.com/user-attachments/assets/67ceeeb7-6a64-4275-9c55-b47aeac64ed8">

Each model provided an overview on the use cases and sample python code. This model is probably better suited for more complex images, instead of using a simple chat box. 

<img width="659" alt="image" src="https://github.com/user-attachments/assets/9d7490f6-d981-40b3-80c6-f22806968f06">

### Azure AI Vision ###

 I created an Azure AI service which then led me to open a new window into Azure AI Studio. 

<img width="802" alt="image" src="https://github.com/user-attachments/assets/f6901dc3-bc53-489a-973a-29c845daa4da">

<img width="916" alt="image" src="https://github.com/user-attachments/assets/62e25425-fbf0-4765-8dc9-413a2666c7cd">

It was easy to navigaate and see what services were available to test out. I selected the 'Vision and Document' tab to see what models were available. 

<img width="902" alt="image" src="https://github.com/user-attachments/assets/1b37d1e3-de6b-444b-b8d1-5338c97abe9c">

Similar to GCP, they had different 'ready-to-use' tasks. I selected the 'read' portion to test out the image extraction 

<img width="748" alt="image" src="https://github.com/user-attachments/assets/b59dd608-195e-432f-894f-c93eb5b4108f">

To upload and run the file, I had to first create a hub to connect with the resource I had created previously in Azure. 

<img width="841" alt="image" src="https://github.com/user-attachments/assets/21af1cbf-99b2-4252-8ab2-36de36d30c9a">

I was orginally going to use a simple image but seeing the samples provided (A healthcare newsletter, resume, etc), I deicded to reuse the text heavy image. 

<img width="733" alt="image" src="https://github.com/user-attachments/assets/0d7325a6-e0ab-4d91-8386-af9e3910d0cc">

I was expecting a similar format to GCP but instead Azure AI Studio was able to extract each text on the page, which I prefered over the breakdown GCP had produced. 

<img width="775" alt="image" src="https://github.com/user-attachments/assets/d59473d7-f559-4528-8af9-e29ca6b89e08">

I also liked was the 'analyze options' tool and the JSON result code provided after the transcription.

<img width="506" alt="image" src="https://github.com/user-attachments/assets/f21b8093-924a-4571-bb47-9d8f87e58287">

<img width="422" alt="image" src="https://github.com/user-attachments/assets/e77f491d-897f-4ff7-b2a9-6dab32963cff">

I decided to check out the speech models on Azure as well.

When I accessed the speech service from Azure, without having to go through the AI Studio, it led me directly to the speech studio where I could upload an audio file and have it transcribed. The transcription was accurate, and suprisngly included the periods at the end of each phrase. 

<img width="810" alt="image" src="https://github.com/user-attachments/assets/2d01e388-13b0-4a97-b57f-a4cd8419182f">

<img width="833" alt="image" src="https://github.com/user-attachments/assets/68027efb-0ed7-4676-b5b9-80fb113841c7">

When looking around in the Azure AI Studio, there was also a speech service available. This one was also accurate and after uploading the file, I didn't even have to press a submit button or play the audio. The transcription was provided seconds after the upload was completed. 

<img width="875" alt="image" src="https://github.com/user-attachments/assets/7b7215df-ea0e-44f5-9348-bae59689f185">

I did find it interesting that I could create a specific speech service through Azure and then also create an AI service where I could perform the same task in the Azure AI Studio. I tried searching online if there was a difference between the two, but it seems like it's more of a service and pricing varation. Regardless of which one you access first, both models use AI. 

