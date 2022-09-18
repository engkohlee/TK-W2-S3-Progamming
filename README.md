import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
                // Membuat Variabel jumlah orang dan nama pemesan
                Byte jumlahOrang;
                String namaPemesan;

                // Harga makanan
                float nasiGoreng    = 9999.99f;
                float ayamBakar     = 12345.67f;
                float steakSirloin  = 21108.40f;
                float kwetiawSiram  = 13579.13f;
                float kambingGuling = 98765.43f;


                Scanner input = new Scanner(System.in);

                System.out.println("Selamat Siang ...");

                System.out.print("Pesan untuk berapa orang : ");
                jumlahOrang = input.nextByte();
                System.out.print("Pesanan atas nama : ");
                namaPemesan = input.next();
                System.out.println();

                System.out.println("Menu Spesial Hari Ini");
                System.out.println("=====================");
                System.out.println("\t1. Nasi Goreng Spesial        @ Rp." + nasiGoreng);
                System.out.println("\t2. Ayam Bakar Spesial         @ Rp." +  ayamBakar);
                System.out.println("\t3. Steak Sirloin Spesial      @ Rp." + steakSirloin);
                System.out.println("\t4. Kwetiauw Siram Spesial     @ Rp." + kwetiawSiram);
                System.out.println("\t5. Kambing Guling Spesial     @ Rp." + kambingGuling);
                System.out.println();

                System.out.println("Pesanan Anda [batas pesanan 0-10]");
                System.out.print("1. Nasi Goreng Spesial    = ");
                Byte pesanNasiGoreng = input.nextByte();
                System.out.print("2. Ayam Bakar Spesial     = ");
                Byte pesanAyamBakar = input.nextByte();
                System.out.print("3. Steak Sirloin Spesial  = ");
                Byte pesanSteak = input.nextByte();
                System.out.print("4. Kwetiauw Siram Spesial = ");
                Byte pesanKwetiaw = input.nextByte();
                System.out.print("5. Kambing Guling Spesial = ");
                Byte pesanKambing = input.nextByte();
                System.out.println();

                System.out.println("Selamat menikmati makanan anda ...");
                System.out.println();

                float totalNasiGoreng = pesanNasiGoreng * nasiGoreng;
                float totalAyamBakar = pesanAyamBakar * ayamBakar;
                float totalSteakSirloin = pesanSteak * steakSirloin;
                float totalKwetiauwSiram = pesanKwetiaw * kwetiawSiram;
                float totalKambingGuling = pesanKambing * kambingGuling;

                System.out.println("Pembelian :");
                System.out.println();
                System.out.println("1. Nasi Goreng Spesial      " + pesanNasiGoreng + " porsi * Rp. " + nasiGoreng      + "\t= Rp. " + totalNasiGoreng );
                System.out.println("2. Ayam Bakar Spesial       " + pesanAyamBakar  + " porsi * Rp. " + ayamBakar       + "\t= Rp. " + totalAyamBakar);
                System.out.println("3. Steak Sirloin Spesial    " + pesanSteak      + " porsi * Rp. " + steakSirloin    + "\t= Rp. " + totalSteakSirloin);
                System.out.println("4. Kwetiauw Siram Spesial   " + pesanKwetiaw    + " porsi * Rp. " + kwetiawSiram    + "\t= Rp. " + totalKwetiauwSiram);
                System.out.println("5. Kambing Guling Spesial   " + pesanKambing    + " porsi * Rp. " + kambingGuling   + "\t= Rp. " + totalKambingGuling + " +");

                System.out.println("=================================================================================");

                double totalPembelian = totalNasiGoreng + totalAyamBakar + totalSteakSirloin + totalKwetiauwSiram + totalKambingGuling;
                System.out.print("Total Pembelian  \t\t\t\t\t\t = Rp. ");
                System.out.printf("%.2f\n", totalPembelian);

                System.out.println("");

                double diskon = totalPembelian *10 /100;
                System.out.print("Disc. 10% <Masa Promosi> \t\t\t\t = Rp."  );
                System.out.printf("%.2f\n", diskon);
                System.out.println("=================================================================================");

                double totalHarga = totalPembelian - diskon;
                System.out.print("Total Pembelian setelah disc 10%  \t\t\t = Rp.");
                System.out.printf("%.2f\n", totalHarga);


                double hargaPerOrang = totalHarga / jumlahOrang;


                System.out.print("Pembelian per orang <untuk " + jumlahOrang + " orang>  \t\t = Rp."  );
                System.out.printf("%.2f\n", hargaPerOrang);


                System.out.println();
                System.out.println("\t\t\t\t\t\t\tTerima kasih atas kunjungan Anda...");
                System.out.println("\t\t\t\t\t\t\t...tekan ENTER untuk keluar...");

            }
        }




