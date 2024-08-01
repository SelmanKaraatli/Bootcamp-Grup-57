# **Takım İsmi**

Flutter Grup 57

# Ürün İle İlgili Bilgiler

## Takım Elemanları


- Yiğitcan Yıldız: Scrum Master, Product Owner



## Ürün İsmi

Köpek Dostu

## Ürün Açıklaması

- Köpek Dostu uygulaması köpek bakımı hakkında blog yazısı içermektedir.

## Ürün Özellikleri 

- Köpek Dostu uygulamasında köpek bakımı hakkında kullanıcılar öğrenmek istedikleri konu hakkında yazıların butonlarına tıklayarak köpek bakımı hakkında bilgi sahibi olabilecekler


## Hedef Kitle

- Evde köpek besleyen kişiler
- Köpekler hakkında bilgi öğrenmek isteyenler
- Köpekleri sevenler
# Sprint 1
**Sprint Notları**:
- Ekip değişikliğinden ve sınav haftasından ötürü ekip zamanında toplanamadı.
- Ekip içi Temmuz ayının 6’sında ve 7’sinde iki toplantı gerçekleştirildi.
- Toplantılarda uygulama fikri ve kullanılacak materyaller belirlendi. 
- Ekip içi görev dağılımları gerçekleştirildi.
 
**Daily Scrum**:
- Daily Scrum'lar için Google Meet platformunun kullanılması kararlaştırılmış ve ortalama 1 saat sürmesi ön görülmüştür.
- Daily Scrum çıktıları için WhatsApp üzerinden iletişimde kalınmasında mutabık olunmuştur.

**Sprint içinde tamamlanması tahmin edilen puan**:150

**Puan tamamlama mantığı**:Proje boyunca tamamlanması gereken 500 puanlık bir backlog'a karar verilmiştir. İlk sprint için 150 puanlık bir ilerleme olması gerektiği ön görülmüştür.


**Sprint board screenshotları**
- Sprint takip aracı olarak Trello kullanımına karar verilmiştir.
![trello](https://github.com/SelmanKaraatli/Bootcamp-Grup-57/assets/65602267/a19c3d61-37a2-4e13-bb29-6177c70e7653)


**Ürün Durumu**: Ekran görüntüleri:


**Sprint Review**: NoteLog'un arayüz ve veritabanı entegrasyonu gibi teknik hedeflerinin 2. sprinte aktarılmasına karar verilmiştir. Yapay zeka tarafında kullanılacak API'lar da yine 2. sprintin ana hedeflerinden birisi olarak belirlenmiştir. Dokümantasyon sürecinde yapılabilecek farklı çalışmalar da yine tartışılmak ve araştırılmak üzere 2. sprinte aktarılmıştır.
**Sprint Review Katılımcıları**: Emre Ataman, Yiğitcan Yıldız, Emir Selman Karaatlı

**Sprint Retrospective**: 1. sprintte elde edilen ilerlemeden genel anlamda memnun kalındı, fakat görüşme sıklığının artması gerektiğine karar verildi. Arayüz tarafında da yenilikçi bir tasarım noktasında hemfikir olundu. Kod tarafında developer'lara daha fazla destek olunması yönünde karar kılındı.

# Sprint 3
**Sprint Notları**:
- Takımımız dağıldı, bu yüzden uygulama fikrimiz değişti, takımda yalnızca tek kişi kaldı.
- Yiğitcan Yıldız dışında diğer arkadaşlarımızın projede bir katkısı bulunmamıştır.
- Yeni uygulama fikri belirlendi ve kodlamaya geçildi.

**Daily Scrum**:
- Takımda tek kişi kaldığından iletişime gerek kalmadı.

**Sprint içinde tamamlanması tahmin edilen puan**: 150 puan

**Puan tamamlama mantığı**: Tüm projeye 3.sprintte başlandığı için 150 puanlık bir proje boyutu belirlendi. Bu sprintte projenin tamamı olan 150 puanın tamamlanması öngörüldü.

**Sprint board screenshotları**
- Sprint takip aracı olarak Trello kullanımına karar verilmiştir.
![Screenshot_29](https://github.com/user-attachments/assets/cef23000-a5af-45b1-a2a6-090c97999753)

**Ürün Durumu**: Ekran görüntüleri:
![Screenshot_29](https://github.com/user-attachments/assets/49ef2662-3128-49cc-bf20-509206858c92)
![Screenshot_31](https://github.com/user-attachments/assets/f999e92c-8b3f-42f4-91f1-1e550457370d)
![Screenshot_33](https://github.com/user-attachments/assets/69057463-2310-4e89-9e6d-6358b225bd0e)
![Screenshot_34](https://github.com/user-attachments/assets/98bcfccb-460e-44b2-8f9d-703c5f0dbfb3)
![Screenshot_35](https://github.com/user-attachments/assets/7e929e34-26c8-4056-85b2-72f645b4ea35)

**Sprint Review**: Takım dağıldığı için geri bildirim verilemedi. Ürünün son aşamasına geldiğimizde uygulamanın ilerleyen aşamalarında blog yazılarının içeriiklerinin çeşitlerinin artırılmasına karar verildi.

**Sprint Review Katılımcıları**: Yiğitcan Yıldız

**Sprint Retrospective**: Uygulamada yapay zeka destekleri olabilirdi. Genel olarak ilerlemeden memnun kalındı. Yenilikçi tasarımlarla uygulama daha fazla zengileşebilirdi.

**Uygulamanın Kodları***

import 'package:flutter/material.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: "Köpek Dostu",
      theme: ThemeData(
        primarySwatch: Colors.blue,
      ),
      home: HomeScreen(),
    );
  }
}

class HomeScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text("Köpek Dostu"),
      ),
      body: BlogScreen(),
    );
  }
}

class BlogScreen extends StatefulWidget {
  @override
  _BlogScreenState createState() => _BlogScreenState();
}

class _BlogScreenState extends State<BlogScreen> {
  String blogContent = 'Kürklü Dostlarımızın Yanındayız';

  void showMarchContent() {
    setState(() {
      blogContent = '''
Yeni köpek sahipleri için temel bakım ipuçları: 1. Beslenme: Kaliteli mama ve taze su sağlayın. 2. Egzersiz: Günde iki kez yürüyüş yapın. 3. Temizlik: Köpeğinizi düzenli olarak yıkayın ve tüylerini tarayın. 4. Sağlık Kontrolleri: Düzenli veteriner ziyaretleri yapın. 5. Eğitim: Temel komutlar ve sosyalleşme için eğitim verin. Bu adımlar, köpeğinizin sağlıklı ve mutlu kalmasını sağlar.
''';
    });
  }

  void showAprilContent() {
    setState(() {
      blogContent = '''
Köpeğinizin Sağlıklı Kalması İçin 10 İpucu
Köpeğinizin sağlıklı ve mutlu bir yaşam sürmesi için dikkat etmeniz gereken önemli noktalar:
Köpeğinizin sağlığı için bu basit ipuçlarına dikkat edin: 1. Dengeli Beslenme: Kaliteli mama seçin. 2. Taze Su: Her zaman temiz su sağlayın. 3. Egzersiz: Günlük yürüyüşler ve oyunlar yapın. 4. Aşılar: Gereken aşıları yaptırın. 5. Parazit Kontrolü: Düzenli parazit önlemleri alın. 6. Tüy Bakımı: Tüylerini tarayın. 7. Diş Bakımı: Dişlerini fırçalayın. 8. Tırnak Kesimi: Tırnaklarını kesin. 9. Veteriner Kontrolleri: Yılda bir sağlık kontrolü yaptırın. 10. Sevgi ve İlgi: Köpeğinize zaman ayırın.''';
    });
  }

  void showMayContent() {
    setState(() {
      blogContent = '''
Köpeklerde Davranış Problemleri ve Çözümleri
Aşırı Havlama: Tetikleyicileri belirleyip olumlu pekiştirme kullanın. Eğitim ve egzersizle enerjisini atmasını sağlayın.

Saldırganlık: Sebepleri belirleyip profesyonel eğitimle sosyalizasyon sağlayın.

Ayrılık Kaygısı: Yalnız kalmaya alıştırın, oyuncaklar ve ödüllerle dikkatini dağıtın.

Çiğneme ve Tahrip Etme: Çiğneme oyuncakları verin, uygun yönlendirme yapın.

Tuvalet Eğitimi: Düzenli rutini ve ödüllendirmeyi kullanın, sabırlı ve tutarlı olun.
''';
    });
  }

  void showJuneContent() {
    setState(() {
      blogContent = '''
Köpekler İçin Evde Hazırlanabilecek Sağlıklı Tarifler
Köpeğiniz için evde sağlıklı mama hazırlamak kolaydır. Havuç ve Tavuk Topları: Haşlanmış tavuk göğsü ve rendelenmiş havuç karıştırın, küçük toplar yapın ve fırında pişirin. Yaban Mersini Buz Küpleri: Yaban mersinini ezip suyla karıştırın, buz kalıplarında dondurun. Bu basit tarifler köpeğinizin sağlığını destekler ve lezzetli bir ödül sunar.
''';
    });
  }

  @override
  Widget build(BuildContext context) {
    return Container(
      padding: EdgeInsets.all(16.0),
      child: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: <Widget>[
            Text(
              blogContent,
              style: TextStyle(fontSize: 18.0),
            ),
            SizedBox(height: 20.0),
            ElevatedButton(
              onPressed: showMarchContent,
              child: Text("Yeni Köpek Sahipleri İçin Temel Bakım Rehberi"),
            ),
            SizedBox(height: 10.0),
            ElevatedButton(
              onPressed: showAprilContent,
              child: Text("Köpeğinizin Sağlıklı Kalması İçin 10 İpucu"),
            ),
            SizedBox(height: 10.0),
            ElevatedButton(
              onPressed: showMayContent,
              child: Text("Köpeklerde Davranış Problemleri ve Çözümleri"),
            ),
            SizedBox(height: 10.0),
            ElevatedButton(
              onPressed: showJuneContent,
              child: Text("Köpekler İçin Evde Hazırlanabilecek Sağlıklı Tarifler"),
            ),
          ],
        ),
      ),
    );
  }
}







