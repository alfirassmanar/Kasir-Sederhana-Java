/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package kasirwarungberas;
import java.util.Scanner;;
/**
 *
 * @author alfir
 */
public class KasirWarungBeras {
//rass
    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        
//      
        Scanner sc = new Scanner(System.in);
        
        int namabarang;
        float jumlahberas;
        float pembayaran;
        int hargaberas = 12000;  
        int stok = 50;
        double diskon;
       
        System.out.print("(inputkan 1 bila ingin membeli Barang)  : ");
        namabarang = sc.nextInt();
        
        if(namabarang == 1){
            System.out.println("\nHarga Beras di Toko Kami         : Rp" + hargaberas + "/Kg");
            System.out.println("Stok Barang                      : " + stok + "Kg");
        } else if(namabarang == 1){
            System.out.println("\nInputkan yang benar");
            System.out.print("Halo jika beli inputkan 1        : ");
            namabarang = sc.nextInt();
        }
//rass
        
       System.out.println("\n----------------------Selamat Datang di Toko Sukamaju Agen Beras-----------------------");
       
        System.out.print("\nMau Beli Berapa (kg)              : "); 
        jumlahberas = sc.nextInt();
        
         if (jumlahberas < 50) {   
             System.out.println("Anda Membeli Beras                : " + jumlahberas + "Kg");
        } else if (jumlahberas > 50 ) {
          System.out.println("Mohon Maaf Stok Beras tidak mencukupi Silahkan Transaksi Lagi");
          
          System.out.print("Mau Beli Berapa (kg)              : "); 
        jumlahberas = sc.nextInt();
    }
//rass        
        float hargatotal = hargaberas*jumlahberas;
        diskon = hargatotal * 0.05;
//rass       
        System.out.println("Harga Beli Beras                  : Rp" + hargatotal);
        System.out.println("Anda Mendapatkan Diskon           : 5%");
 //rass      
        double totalbiaya = hargatotal-diskon;
//        System.out.println("Total                             : Rp" + totalbiaya);
        
        System.out.println("\n------------------Pembayaran---------------------");
            System.out.println("Tagihan Anda                Rp: " + totalbiaya);
            System.out.print("\nMasukan Nominal Uang        Rp: ");
            pembayaran = sc.nextFloat();
//rass            
            double kembalian = pembayaran - totalbiaya;
//rass            
            if(pembayaran > totalbiaya){
                System.out.println("Kembalian Anda                Rp: " + kembalian);
                System.out.println("\nTransaksi Sukses Happy Shoping :)");
            } else if(pembayaran < totalbiaya) {
                System.out.println("----------------------");
                System.out.println("Uang Anda Kurengg Bos!!!");
                System.out.println("----------------------");
                System.out.print("Masukan Nominal Uang        Rp: ");
                pembayaran = sc.nextFloat();
                System.out.println("Kembalian Anda             Rp: " + kembalian);
                System.out.println("\nTransaksi Sukses Happy Shoping :)");
            }
             
  //rass             
            
                    
    }
    
}
