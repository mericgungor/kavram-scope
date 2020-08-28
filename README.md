# kavram-scope
Kavram - Yetki Kapsamı (Scope)\
Bu yazı, yazılım dilinden bağımsız, yazılımcılara hitap etmektedir. Yazılıma başlamadan önce analiz yapan yazılımcılardan iseniz bu yazı size göre. Devam edin.\
Kullanıcı yönetiminde rol kavramını duymuşsunuzdur. Örneğin; "Kullanıcı, Admin rolünde ise şu modüle girebilsin, değilse giremesin" denilebiliyor. Bir kullanıcıya birden fazla rol tanımlanabiliyor ve bu rollere göre yetkilendirme yapılabiliyor.\
Microsoft Membership ve yeni nesil Identity Model alt yapılarını kullanmışsanız kullanıcılar (users) - roller (roles) ikilisini görmüş ve uygulamışsınızdır. Bu yapıların atladığı bir kavram var: "KAPSAM".\
Bu yazıda belki bir çok yazılımcının zaten bildiği ve uyguladığı kapsam (scope) kavramı anlatılmaktadır.\
Kapsam kavramı, telefon şebekelerinin kapsama alanından biliniyor olabilir. Aynı mantıkla, kullanıcıların, rollerinin yanı sıra kapsama alanının da belirlenmesi gerekmektedir. Kapsam tanımlanmazsa, rol tanımı tek başına eksik kalmaktadır./
Konuyu biraz daha açalım; Yönetici, Bölge Müdürü ve Şube Müdürü rolleriniz olsun. Ankara Şube Müdürü diğer illerin verilerini görebilmeli midir? Hayır, görememelidir. Her şube müdürü, kendi ilinin verilerini görebilmelidir. Bölge Müdürü, Ankara, Eskişehir ve Kırıkkale illerinin verilerini görebilmesi gerekiyorsa, bir kullanıcıya birden fazla il tanımı yapılabilmelidir.\

Kullanıcı - Kapsam 1-n ilişki şeması Kullanıcı 1-N kapsam ilişkisi şu demek: Bir kullanıcının bir veya birden fazla kapsamı olabilir, hiç kapsamı olmayabilir.\

Kullanıcı-Kapsam Örnek Veriİsteğe ve projeye bağlı bir dipnot:\
Eğer rol ve kapsam tablolarını sınırsız alt roller ve alt kapsamlar şeklinde tanımlarsanız, dadından yenmez. Örneğin Ankara kapsamında olan bir kullanıcı, Çankaya ve Sincan ilçelerini görebilirsin. Bölge Müdürü rolü olan bir kullanıcı Şube Müdürü rolünü de kullanabilsin.
