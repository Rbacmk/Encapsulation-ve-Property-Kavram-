# Encapsulation-ve-Property-Kavram-
// Encapsulation ve Property Kavramı
            // Kapsülleme :Örneğin siz bir propery yani özellik tanımı yaptınız ve diğer sınıflar içerisinden erişilsin ama sadece okumak için erişilsin değeri dışarıdan değiştirilemesin istiyorsunuz bunu kapsülleme yaparak sağlayabilirsiniz. 
            Student student= new Student(); // Nesnesini oluşturuyoruz.
            student.Isim = "Rabia Çakmak";
            student.SınıfAtlat();



        }
    }
    class Student// Öğrenci adında bir sınıf oluşturuyoruz.
    {
        private string isim;
        private string soyismi;
        private int ogrencıNo;
        private int sınıf;


        public string Isim { get => isim; set => isim = value; }// Property
        public string Soyismi { get => soyismi; set => soyismi = value; }
        public string OgrencıNo { get => ogrencıNo; set => ogrencıNo = value; }
        public string Sınıf { get => sınıf; set => sınıf = value; }
    // Daha Okunabilir haliyle yazalım.
    // get { return isim;}
    // set { isim = value;}
    public Student(string isim,string soyisim, int ogrenciNo, int sınıf)
        {
          İsim = isim;
            soyisim = soyisim;
            ogrenciNo= ogrenciNo;
            Sinif = sınıf;

        }
    public Student() { }// Bos kurucunu oluşturduk.


    }
    // öğrenci bilgilerini geri döndüren metot.
    public void OgrencıBilgileriniGetir()
    {
        Console.WriteLine("Ogrencinin Adı:{0}", this.Isim);
    }
    // Sınıf atlattırmak istediğim öğrenci için
    public void SınıfAtlat()
    {
        this.Sinif = this.Sinif + 1;
    }
    // Sınıf düşürmek için.
    public void SınıfDüsür()
    {
        this.Sinif = this.Sinif - 1;
    }

}
