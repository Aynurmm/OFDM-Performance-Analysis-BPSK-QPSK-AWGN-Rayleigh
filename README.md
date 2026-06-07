Proje Hakkında
Bu çalışma, Orthogonal Frequency Division Multiplexing (OFDM) sisteminin farklı kanal koşulları ve modülasyon teknikleri altındaki performansını karşılaştırmalı olarak analiz eden bir yüksek lisans projesidir.
Modern kablosuz iletişim sistemlerinde (Wi-Fi, 4G LTE, 5G) yaygın olarak kullanılan OFDM tekniği, yüksek hızlı veri iletiminde ortaya çıkan Semboller Arası Girişim (ISI) ve frekans seçici sönümleme problemlerini çözmek amacıyla geliştirilmiştir. Bu projede OFDM sisteminin performansı iki farklı kanal modeli ve iki farklı modülasyon tekniği kullanılarak simüle edilmiş ve sonuçlar teorik değerlerle karşılaştırılmıştır.
Simülasyon, Python programlama dili kullanılarak Google Colab ortamında gerçekleştirilmiş olup IEEE 802.11a standardı parametreleri benimsenmiştir.

Ne Yapıldı?
Çalışmada iki farklı modülasyon tekniği olan BPSK ve QPSK, iki farklı kanal modeli olan AWGN ve Rayleigh üzerinde test edilmiştir. Bu sayede dört farklı kombinasyon karşılaştırmalı olarak incelenmiştir.
BPSK modülasyonunda her bit ayrı ayrı gönderilir ve iki sembol noktası vardır. Bu yapı sayesinde gürültüye karşı yüksek dayanım sağlanır. QPSK modülasyonunda ise her iki bit tek bir sembol ile taşınır ve dört sembol noktası mevcuttur. Bu sayede BPSK'ya kıyasla iki kat daha yüksek veri hızı elde edilir.
AWGN kanalı, yalnızca Gaussian gürültü içeren ideal bir kanal modelidir. Rayleigh kanalı ise bina yansımaları ve çok yollu yayılımı temsil eden gerçekçi bir modeldir. Bu kanalda sinyal genliği rastgele değişmekte ve bazı anlarda sinyal neredeyse tamamen kaybolmaktadır.

Sistem Parametreleri

Parametre                                Değer
Alt Tasiyici Sayisi (N)                  64
Cyclic Prefix (CP)                       16
Pilot Tasiyici                           4
Veri Tasiyici                            60
OFDM Sembol Sayisi                       500
SNR Araligi                              -4 dB ile 25 dB
Modulasyon                               BPSK, QPSK
Kanal                                    AWGN, Rayleigh


Simülasyon Nasil Calisir?
Simülasyon her SNR değeri için şu adımları tekrarlar:

Rastgele bit dizisi üretilir
Seçilen modülasyon tekniğine göre semboller oluşturulur
OFDM çerçevesi kurulur ve IFFT uygulanır
Cyclic Prefix eklenir
Sinyal seçilen kanal modelinden geçirilir
Cyclic Prefix çıkarılır ve FFT uygulanır
Demodülasyon yapılır
Gönderilen ve alınan bitler karşılaştırılarak BER hesaplanır

Her kombinasyon için ayrıca teorik BER formüllerinden elde edilen değerler de hesaplanmış ve simülasyon sonuçları ile karşılaştırılmıştır.

Elde Edilen Sonuçlar
Yapılan simülasyonlar sonucunda aşağıdaki bulgular elde edilmiştir:

SNR arttıkça tüm kombinasyonlarda BER azalmaktadır.
AWGN kanalı, Rayleigh kanalına göre çok daha iyi performans göstermektedir.
Rayleigh kanalında çok yollu yayılım ve sönümleme etkileri BER'i önemli ölçüde artırmaktadır.
BPSK, her iki kanalda da QPSK'ya kıyasla daha düşük hata oranı üretmektedir.
QPSK ise AWGN kanalında BPSK ile benzer BER değeri verirken iki kat daha fazla veri taşımaktadır.
Teorik BER formülleri ile simülasyon sonuçları birbiriyle yüksek doğrulukta örtüşmektedir.

Genel performans sıralaması en iyiden en kötüye doğru şu şekildedir: BPSK+AWGN, QPSK+AWGN, BPSK+Rayleigh, QPSK+Rayleigh.

Kullanilan Araclar

Python 3
Google Colab
NumPy
Matplotlib
SciPy
