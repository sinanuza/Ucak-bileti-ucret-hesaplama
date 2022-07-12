# Ucak-bileti-ucret-hesaplama
www.patika.dev  Ucak Bileti Hesaplama


        public class Ucak_Bileti {
        public static void main(String[] args) {
        int mesafe, yas;
        double toplam=0;
        int sec;
        Scanner input = new Scanner(System.in);
        System.out.println("lutfen yasinizi giriniz:");
        yas = input.nextInt();
        System.out.println("lutfen KM bilgisi giriniz:");
        mesafe = input.nextInt();
        System.out.println("lutfen tek yon icin '1'i, cift yon icin '2' giriniz:");
        sec = input.nextInt();
        if (mesafe > 0) {
            switch (sec) {
                case 1:
                    if ((yas < 12) && yas >= 0) {
                        toplam = 0.10 * mesafe * 0.5;
                    } else if ((yas > 12) && (yas < 24)) {
                        toplam = 0.10 * mesafe * 0.9;
                    } else if (yas > 65) {
                        toplam = 0.10 * mesafe * 0.7;
                    }
                        break;
                case 2:
                    if ((yas < 12) && yas >= 0) {
                        toplam = 0.10 * mesafe * 0.5 * 0.8*2;
                    } else if ((yas > 12) && (yas < 24)) {
                        toplam = 0.10 * mesafe * 0.9 * 0.8*2;
                    } else if (yas > 65) {
                        toplam = 0.10 * mesafe * 0.7 * 0.8*2;
                    }
                        break;
            }System.out.println("Toplam Ucret:"+toplam);
        } else {
            System.out.println("Hatali islem!!");
        }
    }
}
