## Önce Datasetini hazırlayarak başlayalım
##### Youtube'dan farklı farklı uav videolarından toplam 200 adet olacak şekilde ekran görüntüsü aldım.(Proje sadece deneme amaçlı büyük projeler için en az 10000 görüntü olması bence daha iyi sonuçlar verir)
#### Etiketleme
##### Daha sonra bu görüntüleri yolo modellerine uygun bir şekilde etiketlemem gerekiyordu, bu yüzden https://roboflow.com/ sitesinden yararlandım. Burada tek tek görüntüleri kare çerisine alarak etiketleme işlemi gerçekleştirdim.

#### Verileri Ön İşleme
![preprocessing](https://github.com/Leylaleyn/UAV_Detection/assets/96663646/750e3728-ca90-406f-b261-5b11e52cceba)

##### Devamında Roboflow sitesinin sağladığı bir diğer faydalı özelliklerinden olan veri boyutunu ayarlama, veri arttırımı, otomatik train-test-valid ayarlamasını gerçekleştirdim. Bu sayede verilerim toplam 520 adet oldu.
##### %70 train, %20 validation, %10 test için ayrıldı.

##### Not: Ben kodlarımı google colab ortamında çalıştırdım. Roboflow ile uyumlu yolo kodlarını incelemek isterseniz:
https://colab.research.google.com/github/roboflow-ai/notebooks/blob/main/notebooks/train-yolov8-object-detection-on-custom-dataset.ipynb

https://colab.research.google.com/github/roboflow-ai/notebooks/blob/main/notebooks/train-yolov9-object-detection-on-custom-dataset.ipynb?ref=blog.roboflow.com

## Modelleme Aşaması
##### Deneme ve karşılaştırma amaçlı 2 Model tercih ettim: Yolov8 ve Yolov9
YOLOV8 Modeli:
![image](https://github.com/Leylaleyn/UAV_Detection/assets/96663646/dc4e28ac-8ed1-4d22-bf3d-cb0234713c77)
Sonuçlar:
![image](https://github.com/Leylaleyn/UAV_Detection/assets/96663646/1849db74-303e-403b-bebb-4cb7be7635d2)
![image](https://github.com/Leylaleyn/UAV_Detection/assets/96663646/6bc346ac-12ba-4cdb-a200-dc1b46e631ce)
![val_batch1_labels](https://github.com/Leylaleyn/UAV_Detection/assets/96663646/5b1483ef-d514-40c1-ae20-288f8bb7ae99)

YOLOV9 Modeli:

![image](https://github.com/Leylaleyn/UAV_Detection/assets/96663646/f7efa9d8-bffc-4e05-b157-9a14fbf6d074)


Sonuçlar:


![image](https://github.com/Leylaleyn/UAV_Detection/assets/96663646/6140aa5f-61b7-4839-9ead-86e97de1ef5e)

![image](https://github.com/Leylaleyn/UAV_Detection/assets/96663646/afa2faec-8ee5-4950-943d-6a1919b4ce1c)
![val_batch0_pred](https://github.com/Leylaleyn/UAV_Detection/assets/96663646/d080d1b5-b2ab-4c9e-a6de-837adc760e76)



