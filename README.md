# -ATM-Projesi
projedeki ATM işlemlerini "Switch-Case" kullanarak yapınız.

    import java.util.Scanner;

    public class Main {
    public static void main(String[] args) {
        String userName, password;
        Scanner inp = new Scanner(System.in);
        int right = 3;
        int balance = 1500;
        int select,price;
        while (right > 0) {
            System.out.print("Kullanıcı Adınız :");
            userName = inp.nextLine();
            System.out.print("Şifre Giriniz :");
            password = inp.nextLine();
            if (userName.equals("patika") && password.equals("dev123")) {
                System.out.println("Merhaba, Kodluyoruz  bankasına Hoşgeldiniz");
                do {

                    System.out.println("1- Para yatırma\n" +
                            "2-Para çekme\n" +
                            "3-Bakiye Sorgula\n" +
                            "4-Çıkış yap");
                    System.out.print("Lütfen yapmak istediğiniz işlemi seçiniz :");
                    select = inp.nextInt();
                  switch (select){
                      case 1:
                          System.out.print("Yatırmak istediğiniz para miktarı :");
                           price=inp.nextInt();
                          balance+=price;
                          break;
                      case 2:
                          System.out.print("Çekmek istediğiniz para miktarı");
                          int price2=inp.nextInt();
                          if (balance<price2){
                              System.out.println("Yetersiz Bakiye");

                          }else {
                              balance-=price2;
                          }
                          break;
                      case 3:
                          System.out.println("Bakiyeniz : " + balance);
                          break;
                  }
                } while (select != 4);
                System.out.println("Tekrar görüşmek üzere :)");
                break;
            } else {
                System.out.println("Hatalı kullanıcı adı veya şifre. Tekrar deneyiniz. ");
                right--;
                if (right == 0) {
                    System.out.println("Hesabınız bloke olmuştur lütfen banka ile iletişime geçiniz.");
                } else {
                    System.out.println("Kalan Hakkınız : " + right);
                }

            }
        }

      }
     }
https://app.patika.dev/ahmetfurkan
