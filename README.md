Proje Hakkında
Bu çalışma, Orthogonal Frequency Division Multiplexing (OFDM) sisteminin farklı kanal koşulları ve modülasyon teknikleri altındaki performansını karşılaştırmalı olarak analiz eden bir yüksek lisans projesidir.
Modern kablosuz iletişim sistemlerinde (Wi-Fi, 4G LTE, 5G) yaygın olarak kullanılan OFDM tekniği, yüksek hızlı veri iletiminde ortaya çıkan Semboller Arası Girişim (ISI) ve frekans seçici sönümleme problemlerini çözmek amacıyla geliştirilmiştir. Bu projede OFDM sisteminin performansı iki farklı kanal modeli ve iki farklı modülasyon tekniği kullanılarak simüle edilmiş ve sonuçlar teorik değerlerle karşılaştırılmıştır.
Simülasyon, Python programlama dili kullanılarak Google Colab ortamında gerçekleştirilmiş olup IEEE 802.11a standardı parametreleri benimsenmiştir.

 Araştırma Soruları
Bu çalışmada aşağıdaki temel araştırma sorularına yanıt aranmıştır:

AWGN ve Rayleigh kanal modelleri altında OFDM sisteminin BER performansı nasıl değişmektedir?
BPSK ve QPSK modülasyon teknikleri arasında hata oranı ve veri hızı açısından nasıl bir denge mevcuttur?
SNR arttıkça sistem performansı nasıl gelişmektedir?
Rayleigh sönümlemesinin OFDM sistem performansı üzerindeki etkisi ne düzeydedir?
Teorik BER formülleri ile simülasyon sonuçları ne ölçüde örtüşmektedir?


 Sistem Parametreleri
Bu çalışmada kullanılan parametreler IEEE 802.11a kablosuz iletişim standardına göre belirlenmiştir.
ParametreDeğerAçıklamaAlt Taşıyıcı Sayısı (N)64FFT/IFFT boyutu — IEEE 802.11aCyclic Prefix (CP)16N/4 — ISI önleme mekanizmasıPilot Taşıyıcı4Kanal tahmini için ayrılan taşıyıcıVeri Taşıyıcısı60N − Pilot = veri iletimiOFDM Sembol Sayısı500İstatistiksel güvenilirlik içinSNR Aralığı−4 … 25 dB1 dB adımlarla — toplam 30 noktaModülasyonBPSK, QPSKİki teknik karşılaştırmalıKanal ModeliAWGN, Rayleighİki model karşılaştırmalı

 Test Senaryoları
Çalışmada toplam 4 farklı kombinasyon test edilmiştir. Her kombinasyon için −4 dB ile 25 dB arasında 30 SNR noktasında simülasyon gerçekleştirilmiştir.
SenaryoModülasyonKanalAçıklamaS1BPSKAWGNReferans senaryo — en iyi BER performansıS2QPSKAWGN2× veri hızı, BPSK ile benzer BERS3BPSKRayleighSönümleme etkisinin BPSK üzerindeki analiziS4QPSKRayleighEn zorlu senaryo — maksimum kanal etkisi
