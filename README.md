 E-Ticaret Uygulaması (Bulut Tabanlı)

## 📌 Proje Tanımı ve Hedefleri

Bu proje, temel **bulut bilişim kavramlarını** içeren modüler ve bulut tabanlı bir **e-ticaret sistemi** geliştirmeyi amaçlamaktadır. Kullanıcılar ürün ekleyebilir, listeleyebilir ve silebilir. Bu işlemler, React.js kullanıcı arayüzü ile etkileşen bir RESTful API üzerinden gerçekleştirilmiştir. Sistem, Google Cloud Platform üzerinde ölçeklenebilir ve güvenli şekilde dağıtılmıştır.

---

## 🛠️ Kullanılan Teknolojiler

| Katman     | Teknoloji                              |
|------------|-----------------------------------------|
| Backend    | Node.js (Express.js Framework)          |
| Frontend   | React.js                                |
| Veritabanı | MongoDB (MongoDB Atlas)                 |
| Bulut      | Google Cloud Platform (App Engine)      |

---

## 🧪 Geliştirme Süreci

### 🔧 3.1 Backend Mimarisi
- Express.js ile ürün CRUD işlemleri için RESTful API geliştirildi.
- MongoDB Atlas bağlantısı yapılandırıldı.
- CORS desteği eklendi, HTTPS ve güvenli başlıklar ile mixed content problemleri önlendi.

### 🎨 3.2 Frontend Geliştirme
- Ürün oluşturma, listeleme ve silme işlemleri için **modüler React bileşenleri** geliştirildi.
- Fetch API ile backend entegrasyonu sağlandı.
- Temel seviyede **responsive tasarım** uygulandı.

### 🔗 3.3 API Entegrasyonu
- RESTful iletişim React <-> Node.js arasında yapılandırıldı.
- CORS politikası ve HTTPS desteği ile güvenli veri alışverişi sağlandı.

---

## ☁️ Bulut Dağıtım Süreci

### 📦 Backend
- Express.js API, **Google App Engine Standard Environment** üzerinde dağıtıldı.
- `app.yaml` dosyası ile servis yapılandırması sağlandı:
  
```yaml
runtime: nodejs18
env: standard
instance_class: F1
automatic_scaling:
  target_cpu_utilization: 0.65
  min_instances: 1
  max_instances: 3
