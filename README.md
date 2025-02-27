# Hafta-2
08.02.2025 Emrah Hocanın dersi 
public class bsınıfı {
// 1'den N'e kadar olan tek ve çift sayıların toplamını veren metot//
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("n sayıyı giriniz: ");
        int n = sc.nextInt();
        Toplam(n);
    }
    public static void Toplam (int n){
        int toplamTek= 0;
        int toplamCift= 0;
        for ( int i= 1; i<= n; i++){
            if (i%2 == 0){
                toplamCift += i;
            }
            else {
                toplamTek += i;
            }
        }
        System.out.println("Çift Sayılar "+ toplamCift);
        System.out.println("Tek Sayılar " + toplamTek);
    }
       ///******************************///
       
//İki sayının toplamını veren metot//
 public static void Toplam ( int a , int b ){
        int toplam1 = a + b;
        System.out.println( "Toplam= " + toplam1 );
    }
    public static void main ( String[] args ){
        Toplam( 10, 20 );
    }

    ///******************************///

//1den N kadar olan sayilarin ortalamasini donduren metot//
   public static double Ortalama ( int n){
        int toplam= 0;
        for ( int i = 0; i <= n; i++){
          toplam +=i;
        }
        double ortalama = (double) toplam/n;
        System.out.println(ortalama);
        return ortalama;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        Ortalama(n);
        double ortalama = Ortalama(n);//!!!!DİKKAT
        System.out.println(ortalama);
    }
    
    ///******************************///
    
 //Bir dizinin elemanlarinin ortalamasını yazdiran metot//
 public static double DiziYazdirma ( int dizi []){
        double toplam = 0;
        for ( int i = 0 ; i < dizi.length ; i++ ){
          toplam += dizi[i];
        }
        double ortalama = toplam / dizi.length;    ///BURDA LENGHT DE DİKKAT ET
       ///return  toplam / dizi.length;// YAZILABİLİR
        return ortalama;
    }
    public static void main ( String[] args ){
        int dizi []= {1 , 3 , 5 , 6 };
        double ortalama = DiziYazdirma(dizi);     ///BU SAYEDE DIŞARDA KULLANABİLİYORUZ
        System.out.println( "B02: "+ ortalama );
    }
    
    ///******************************/// 
    
//Bir dizinin en küçük elamını döndüren metot//
public static int enKucukbulma (int dizi[]){
        //int dizi [] burda tanımlama gerek yok
        int enKucuk = dizi [0];
        for (int i = 1 ;i<dizi.length;i++){      /// int 0 dan değilde anlamlı kod için 1 den başlatılmalı.
            if (enKucuk > dizi[i]){
              enKucuk = dizi[i];
            }
        }
        return enKucuk;
    }
    public static void main ( String[] args ) {
        int dizi[] = {1, 3, 5, 6};
        enKucukbulma(dizi);
        int k = enKucukbulma(dizi);
        System.out.println(k);
    }
    
  ///******************************///
  
    ///Bir dizideki en büyük elamanı bulma metodu///
  public static void enBuyuk ( int dizi []){
      int enBuyuk = dizi[0];
      for (int i = 0; i<dizi.length ; i++){
          if ( enBuyuk < dizi[i]){
              enBuyuk = dizi[i];
          }
      }
      System.out.println(enBuyuk);
  }
  public static void main(String[] args) {
      Scanner inp = new Scanner(System.in);
      int dizi[] = new int [5];
      for (int i = 0; i < dizi.length ; i++){
          dizi[i] = inp.nextInt();
      }
      enBuyuk(dizi);
  }

    ///******************************///

///2 nokta çarpımı yapan metodu (dot product)///
   public static int dotProduct (int v1 [], int v2 []){
        int toplam = 0;
        for (int i = 0; i < v1.length; i++){
            toplam += v1[i]*v2[i];
        }
        //System.out.println(toplam);
        return toplam;
    }
    public static void main ( String[] args ) {
        Scanner sc = new Scanner(System.in);
        int v1[] = new int[3];
        int v2[] = new int[3];
        for (int i = 0; i < v1.length; i++) {
            v1[i] = sc.nextInt();
        }
        for (int i = 0; i < v2.length; i++) {
            v2[i] = sc.nextInt();
        }
        int toplam = dotProduct(v1, v2);
        System.out.println(toplam);
    }
    
 ///******************************///
 
///2 vektör toplamı///
    public static void Vektor ( int v1 [], int v2 []){
        for (int i = 0; i < v1.length; i++){
            System.out.println( v1 [i] + v2 [i]);
        }
    }
    public static void main ( String[] args ){
        Scanner sc = new Scanner (System.in);
        int v1 [] = new int [3];
        int v2 [] = new int [3];
        for (int i = 0; i < v1.length; i++){
            v1[i] = sc.nextInt();
        }
        for (int i = 0; i < v2.length; i++){
            v2[i] = sc.nextInt();
        }
        Vektor ( v1 , v2 );
    }
    
   ///******************************///
   
///Matristeki her satırdaki en küçük elamanları bulan  metot///
    public static void Matris_satır (int dizi [][]){
        for (int i = 0; i < dizi.length; i++) {
           int enKucuk = dizi [i][0];
            for (int j = 0; j < dizi.length; j++) {
             if (enKucuk > dizi[i][j]) {
                 enKucuk = dizi[i][j];
             }
            }
            System.out.println(i+1 + ". Satırdaki en kucuk "+ enKucuk);
        }
    }
    public static void main(String[] args) {
        int [][] dizi = new int [][]{
                {200 , 300, 400},
                {300 , 400, 500},
                {400 , 500, 600}
        };
         Matris_satır(dizi);
         sutun_kucuk(dizi);
    }

// Sütundaki en küçük değeri bulan metot//
     public static void sutun_kucuk ( int dizi [][]){
        for (int j = 0; j < dizi.length; j++) {
            int enKucuk = dizi [0][j];
            for (int i = 0; i < dizi.length; i++) {
                if (enKucuk > dizi[i][j]) {
                    enKucuk = dizi[i][j];
                }
            }
            System.out.println(j+1 + ". Sütunundaki en kucuk "+ enKucuk);
        }

    }

}
}
    





















    
    
