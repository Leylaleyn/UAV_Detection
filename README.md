## Önce Datasetini hazırlayarak başlayalım
##### Youtube'dan farklı farklı uav videolarından toplam 200 adet olacak şekilde ekran görüntüsü aldım.(Proje sadece deneme amaçlı büyük projeler için en az 10000 görüntü olması bence daha iyi sonuçlar veriri)
#### Etiketleme
##### Daha sonra bu görüntüleri yolo modellerine uygun bir şekilde etiketlemem gerekiyordu, bu yüzden https://roboflow.com/ sitesinden yararlandım. Burada tek tek görüntüleri kare çerisine alarak etiketleme işlemi gerçekleştirdim.

#### Verileri Ön İşleme
![preprocessing](https://github.com/Leylaleyn/UAV_Detection/assets/96663646/750e3728-ca90-406f-b261-5b11e52cceba)
##### Devamında Roboflow sitesinin sağladığı bir diğer faydalı özelliklerinden olan veri boyutunu ayarlama, veri arttırımı, otomatik train-test-valid ayarlamasını gerçekleştirdim. Bu sayede verilerim toplam 540 adet oldu.
##### %70 train, %20 validation, %10 test için ayrıldı.
