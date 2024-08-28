# YOLOV10
Bu projede YOLOV10 hakkında bilgi vereceğim ve kurarken aldığım hataları yazacağım. Öncelikle YOLOV10 modeli henüz çıkmadı. Bu [https://github.com/THU-MIG/yolov10](url) sayfadan demo modunu kullanabiliyoruz. Ultralytics in şuan en güncel modeli aslında V8 modelidir. Aşağıdaki grafiklerden de anladığımız kadarıyla en iyi model olacağını da görebiliyoruz.

![latency](https://github.com/user-attachments/assets/a9d9f0da-375f-46fd-aee5-2c9b30f08025)          ![params](https://github.com/user-attachments/assets/559dfc29-3c8b-4d46-818c-1b99ba9efbeb)


### pip install -q git+https://github.com/THU-MIG/yolov10.git
### yolov10n veya farklı bir ağırlığı github reposundan indirebilirsiniz ardından bunu .py dosyasıyla aynı uzantıya getirmelisiniz.

# Modeli yüklerken aldığım hatalar!!!

1-DLL HATASI
![hata_1](https://github.com/user-attachments/assets/cfe46bca-9cca-44c3-9490-51bb240fb0a3)

Bu .dll hatasını aldım ve daha sonra youtubedan bir video buldum. DLL hatası ilgili dosyayı bulamayınca çıkıyormuş. Bu videonun altındaki linkten libomp140.x86_64.dll dosyasını indirin ve daha sonra bunu system32 dosyasına ekleyin.

[https://youtu.be/npPdd7wk3Ok?si=mF2Sn1QGddeSXpIJ](url)

3- HuggingFace HATASI

ModuleNotFoundError: No module named 'huggingface_hub'
Dll hatasından sonra yukarıda ki gibi bir hata aldım. Bunu da huggingface_hub u indirerek çözdüm.

       3.1 pip install huggingface_hub



2- OPENCV HATASI

Bu hata için: Önce opencv yi silip sonra tekrar yükleyeceğiz.
  pip uninstall opencv-python 
  pip install opencv-python

