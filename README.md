# Junio-Plant-Species-Image-Classification-Using-Teachable-Machine
exported file -d/14vpAl https://drive.google.com/file/Mr8haOKU0dHuUNW3aKqYAg8EVvZ/view?usp=drive_link


A. Project Overview
Brief Description of the Project
This project aims to develop an image classification system for mangrove species using Teachable Machine, a web-based tool that leverages machine learning for easy model creation. Users can train the model by providing images of different mangrove species, allowing the system to recognize and classify them accurately. This project helps in biodiversity monitoring, environmental conservation, and educational purposes by enabling quick identification of mangrove species through photos. It also demonstrates how accessible machine learning tools can be applied to ecological studies.

Purpose of the image classification model
The purpose of this image classification model is to automatically identify and differentiate mangrove species from images, providing a fast and accurate way to support environmental monitoring, conservation efforts, and educational activities. It aims to assist researchers, students, and environmentalists in recognizing mangrove species without requiring extensive botanical expertise, making species identification more efficient and accessible.

B. Plant Species Section 












C. MODEL TRAINING DETAILS

<img width="1366" height="768" alt="Screenshot (114)" src="https://github.com/user-attachments/assets/2be7c207-2955-4f76-af04-a276fabfad90" />


<img width="228" height="501" alt="botch" src="https://github.com/user-attachments/assets/acf213de-4760-4258-b1bb-e04a03457036" />

D. MODEL EVALUATION 

<img width="310" height="620" alt="confusion matrix" src="https://github.com/user-attachments/assets/d42f2760-105c-43a6-ae72-8671ec1fafcd" />
<img width="311" height="613" alt="accuracy per class" src="https://github.com/user-attachments/assets/9f21fd4a-9ad7-46da-ad0a-c6f59485f7c0" />
<img width="327" height="543" alt="loss values" src="https://github.com/user-attachments/assets/618996c6-e15f-4d74-a6ad-7ad9b3abf982" />

 E. MODEL TESTING 

 <img width="184" height="483" alt="1" src="https://github.com/user-attachments/assets/8c3170d4-6b1d-48e5-b1c9-1efbb2fd954b" />
<img width="298" height="489" alt="2" src="https://github.com/user-attachments/assets/9a488ee0-0992-49db-893a-0efd88a711c1" />
<img width="156" height="602" alt="3" src="https://github.com/user-attachments/assets/469f6f31-dd86-463c-8b97-28c2fde43bc0" />
<img width="159" height="599" alt="4" src="https://github.com/user-attachments/assets/551f5cbf-935c-4f0e-9e38-b769237a4226" />
<img width="175" height="570" alt="5" src="https://github.com/user-attachments/assets/4d21eceb-13f6-4aff-888d-1a603857e5cf" />
<img width="161" height="479" alt="6" src="https://github.com/user-attachments/assets/879773f0-77ef-4242-988d-456b1a77e4a9" />
<img width="132" height="565" alt="7" src="https://github.com/user-attachments/assets/30845251-21c7-49c2-8d6f-d35675544557" />
<img width="140" height="519" alt="8" src="https://github.com/user-attachments/assets/8e8b9e6d-75d8-444d-9a9b-c425e9ca1784" />
<img width="156" height="383" alt="9" src="https://github.com/user-attachments/assets/16761b3d-2696-4a8d-836d-ea706e4722c1" />
<img width="157" height="436" alt="10" src="https://github.com/user-attachments/assets/4822d6cb-98a0-42c8-a66d-d396926a2dd8" />

REFLECTION QUESTIONS: 

Answer the following questions based on your experience:
1. How did the number of images per class affect your model’s accuracy?


2. Which plant species were most commonly misclassified and why?
 Answer: Rhizophora mucronata ↔ Rhizophora stylosa
Why misclassified:
Very similar prop roots (stilt roots)
Leaves are both elliptical and glossy
Differences (flower size, style length) are not visible in images
👉 The model mostly sees overall shape, not tiny botanical details.

- Bruguiera gymnorhiza ↔ Bruguiera × hainesii
Why misclassified:
Same genus = almost identical leaf shape and color
Hybrid species (B. × hainesii) visually overlaps both parent species
Flowers/fruits (key identifiers) are rarely captured in datasets

- Sonneratia caseolaris ↔ Sonneratia ovata
Why misclassified:
Similar rounded leaves
Both have pneumatophores (breathing roots)
Bark and flower differences are subtle and often excluded from images

- Avicennia officinalis ↔ Lumnitzera littorea
Why misclassified:
Overlapping leaf size and canopy shape
Images Taken from far away hide:
Salt glands (Avicennia)
Flower color (Lumnitzera)

-Acanthus ilicifolius ↔ Wedelia biflora
Why misclassified:
Both are low-growing coastal plants
Similar green leaf dominance
Flowers (spiky vs daisy-like) are not always visible in training images

- Scaevola taccada ↔ Batis maritima (Saltwort)
Why misclassified:
Both found in beachfront/coastal zones
Background similarity (sand, shoreline vegetation)
Leaf texture differences are subtle for beginners’ datasets

- Pongamia pinnata ↔ Erythrina variegata
Why misclassified:
Both are medium to large coastal trees
Similar compound leaves
Trunks and flowers (key differences) often missing in images

- Cynometra ramiflora ↔ Ficus superba
Why misclassified:
Dense foliage and similar tree silhouette
Aerial roots (Ficus) may not appear in cropped images
Leaf venation not easily learned by small models

-Kandelia candel ↔ Rhizophora species
Why misclassified:
All have prop/stilt roots
Similar mangrove habitat and growth form
Seedling differences are rarely captured

-Osbornia octodonta ↔ Scyphiphora hydrophylacea
Why misclassified:
Rare species = few training images
Small leaves + shrubs = low visual uniqueness
Model bias toward more common species


3. How did changing the epochs, batch size, or learning rate affect the training results?
Answer: Increasing the epochs improved accuracy at first, but too many epochs caused overfitting. Using a smaller batch size resulted in more stable learning and better validation accuracy, while larger batches trained faster but reduced generalization. A high learning rate made training unstable, a low learning rate slowed convergence, and a moderate learning rate produced the best and most stable training results.
   
4. What challenges did you encounter during dataset collection and labeling?
Answer: Species like Bruguiera × hainesii and Scyphiphora hydrophylacea had very few available images
Caused class imbalance and biased predictions
 
5.  If you were to improve your model, what specific changes would you make and why?
   Answer: I would improve the model by adding more balanced images (especially for rare mangrove species), applying data augmentation, and using a pre-trained CNN through transfer learning. I would also fine-tune the epochs, batch size, and learning rate and verify image labels carefully. These changes would reduce misclassification of similar species, prevent overfitting, and improve overall accuracy and generalization.
   
