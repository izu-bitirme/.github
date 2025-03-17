##  Welcome to the team 🙌 


### **📌 GitHub Çalışma Akışı ve Branch Stratejisi**

API geliştirme sürecinde **temiz ve yapılandırılmış bir çalışma** sağlamak için aşağıdaki adımları izleyin.

---

### **1️⃣ Her Özellik İçin Yeni Bir Branch Oluşturun**  
Geliştirmeye başlamadan önce, **dev** branch’inden **yeni bir branch oluşturun**:

```bash
git checkout dev  # Development branch'ine geçiş yapın
git pull origin dev  # Son güncellemeleri alın
git checkout -b feature/{özellik_adı}  # Yeni bir özellik branch'i oluşturun
```

**Örnek:**  
**Task Completion API** üzerinde çalışıyorsanız:  
```bash
git checkout -b feature/task-completion-api
```

---

### **2️⃣ Özelliği Geliştirin ve Test Edin**  
✅ **Atanan görevinizi kodlayın**  
✅ **API'nin yerel makinenizde doğru çalıştığından emin olun**  
✅ **Postman ile tüm endpoint'leri test edin**  
✅ **Herhangi bir hata düzeltmesini yapmadan önce commit işlemi yapmayın**  

---

### **3️⃣ Değişiklikleri Commit ve Push Edin**  
Özellik tamamlandı ve test edildiğinde:  

```bash
git add .
git commit -m "✨ Task Completion API Eklendi (#issue_numarası)"
git push origin feature/{özellik_adı}
```

Örnek:  
```bash
git push origin feature/task-completion-api
```

---

### **4️⃣ Pull Request (PR) Oluşturun**  
- **GitHub** üzerinden `feature/{özellik_adı}` branch’ini **dev** branch’ine karşı bir **Pull Request** oluşturun.  
- **Değişikliklerinizi açıklayan net bir yazı** ekleyin ve ilgili issue numarasını belirtin.  
- **Postman test sonuçlarını** ekran görüntüsü veya log olarak ekleyin.  
- En az **bir kişiyi** kod incelemesi için atayın.

---

### **5️⃣ Kod İncelemesi ve Merge İşlemi**  
✅ İnceleme yapan kişi, PR'ı kontrol eder.  
✅ Onay alındıktan sonra **özellik branch’i `dev` branch’ine merge edilir**.  
✅ Merge işlemi sonrası, **özellik branch’i silinir**:  

```bash
git branch -d feature/{özellik_adı}
git push origin --delete feature/{özellik_adı}
```

---

### **🚨 Önemli Kurallar**  
❌ **Doğrudan `dev` branch'ine commit yapmayın** – Her zaman özellik branch’i kullanın.  
❌ **PR oluşturmadan önce API’yi test edin.**  
✅ **Yeni bir branch oluştururken `dev` branch’ini güncellediğinizden emin olun.**  
✅ **Commit mesajlarında mutlaka ilgili issue numarasını belirtin.**  

---

Bu süreç **düzenli işbirliği, temiz kod ve minimum çatışma** sağlamak için oldukça önemlidir. 🚀
