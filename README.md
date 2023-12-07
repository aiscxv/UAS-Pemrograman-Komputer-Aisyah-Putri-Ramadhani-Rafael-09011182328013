# UAS-Pemrograman-Komputer-Aisyah-Putri-Ramadhani-Rafael-09011182328013
Nama: Aisyah Putri Ramadhani Rafael
Nim: 09011182328013
Kelas: SK1A
Ujian: UAS Pemrograman Komputer

1. Diskon
import java.util.Scanner;

public class TokoOnline {

    public static void main(String[] args) {
        // Membuat objek scanner untuk membaca input
        Scanner input = new Scanner(System.in);

        // Membuat variabel untuk menyimpan harga barang, jumlah pembelian, dan diskon
        double harga, jumlah, diskon;

        // Membuat variabel untuk menyimpan total harga sebelum dan sesudah diskon
        double totalSebelum, totalSesudah;

        // Membaca input harga barang dari pengguna
        System.out.print("Masukkan harga barang: ");
        harga = input.nextDouble();

        // Membaca input jumlah pembelian dari pengguna
        System.out.print("Masukkan jumlah pembelian: ");
        jumlah = input.nextDouble();

        // Menghitung total harga sebelum diskon
        totalSebelum = harga * jumlah;

        // Menentukan diskon berdasarkan jumlah pembelian
        if (jumlah < 5) {
            // Jika jumlah kurang dari 5, tidak ada diskon
            diskon = 0;
        } else if (jumlah >= 5 && jumlah <= 10) {
            // Jika jumlah antara 5 hingga 10, diskon 5%
            diskon = 0.05;
        } else if (jumlah >= 11 && jumlah <= 20) {
            // Jika jumlah antara 11 hingga 20, diskon 10%
            diskon = 0.1;
        } else {
            // Jika jumlah lebih dari 20, diskon 20%
            diskon = 0.2;
        }

        // Menghitung total harga sesudah diskon
        totalSesudah = totalSebelum - (totalSebelum * diskon);

        // Menampilkan total harga sebelum dan sesudah diskon
        System.out.println("Total harga sebelum diskon: " + totalSebelum);
        System.out.println("Diskon: " + (diskon * 100) + "%");
        System.out.println("Total harga sesudah diskon: " + totalSesudah);
    }
}

2. Autentikasi
import java.util.Scanner;

public class Autentikasi {
    public static void main(String[] args) {
        // Nilai username dan password yang valid
        String usernameValid = "ais";
        String passwordValid = "songkang";

        // Menggunakan Scanner untuk menerima input dari pengguna
        Scanner scanner = new Scanner(System.in);

        // Meminta pengguna memasukkan username
        System.out.print("Masukkan username: ");
        String usernameInput = scanner.nextLine();

        // Meminta pengguna memasukkan password
        System.out.print("Masukkan password: ");
        String passwordInput = scanner.nextLine();

        // Memeriksa apakah username dan password sesuai dengan nilai yang valid
        if (usernameInput.equals(usernameValid) && passwordInput.equals(passwordValid)) {
            System.out.println("Autentikasi Berhasil");
        } else {
            System.out.println("Autentikasi Gagal");
        }

        // Menutup Scanner
        scanner.close();
    }
}

3. Fibonacci
import java.util.Scanner;

public class Fibonacci {
    public static void main(String[] args) {
        // Menggunakan Scanner untuk menerima input dari pengguna
        Scanner scanner = new Scanner(System.in);

        // Meminta pengguna memasukkan nilai n
        System.out.print("Masukkan nilai n untuk deret Fibonacci: ");
        int n = scanner.nextInt();

        // Menampilkan deret Fibonacci hingga suku ke-n
        System.out.println("Deret Fibonacci hingga suku ke-" + n + ":");
        for (int i = 0; i < n; i++) {
            System.out.print(fibonacci(i) + " ");
        }

        // Menutup Scanner
        scanner.close();
    }

    // Fungsi rekursif untuk menghitung suku ke-n dalam deret Fibonacci
    public static int fibonacci(int n) {
        if (n <= 1) {
            return n;
        } else {
            return fibonacci(n - 1) + fibonacci(n - 2);
        }
    }
}

4. Faktorisasi
import java.util.Scanner;

public class Faktorisasi {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n;

        System.out.print("Masukkan bilangan bulat positif: ");
        n = scanner.nextInt();

        System.out.print("Faktorisasi " + n + ": ");

        for (int i = 2; i <= n; i++) {
            while (n % i == 0) {
                System.out.print(i + " ");
                n /= i;
            }
        }
    }
}

5. Kalkulator
import java.util.Scanner;

public class Kalkulator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int angka1, angka2, hasil;
        char operator;

        System.out.print("Masukkan angka pertama: ");
        angka1 = scanner.nextInt();

        System.out.print("Masukkan operator (+, -, *, /): ");
        operator = scanner.next().charAt(0);

        System.out.print("Masukkan angka kedua: ");
        angka2 = scanner.nextInt();

        switch (operator) {
            case '+':
                hasil = angka1 + angka2;
                System.out.println(angka1 + " + " + angka2 + " = " + hasil);
                break;
            case '-':
                hasil = angka1 - angka2;
                System.out.println(angka1 + " - " + angka2 + " = " + hasil);
                break;
            case '*':
                hasil = angka1 * angka2;
                System.out.println(angka1 + " * " + angka2 + " = " + hasil);
                break;
            case '/':
                hasil = angka1 / angka2;
                System.out.println(angka1 + " / " + angka2 + " = " + hasil);
                break;
            default:
                System.out.println("Operator yang dimasukkan salah!");
                break;
        }
    }
}

6. Palindrom
import java.util.Scanner;

public class Palindrom {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String kata, reverse = "";

        System.out.print("Masukkan kata atau frasa: ");
        kata = scanner.nextLine();

        int length = kata.length();

        for (int i = length - 1; i >= 0; i--) {
            reverse = reverse + kata.charAt(i);
        }

        if (kata.equals(reverse)) {
            System.out.println(kata + " adalah palindrom");
        } else {
            System.out.println(kata + " bukan palindrom");
        }
    }
}

7. Perpustakaan Buku
   public class Buku {
    private String judul;
    private String penulis;
    private int tahunTerbit;
    private boolean tersedia;

    // inisialisasi buku
    public Buku(String judul, String penulis, int tahunTerbit) {
        this.judul = judul;
        this.penulis = penulis;
        this.tahunTerbit = tahunTerbit;
        this.tersedia = true;
    }

    // menampilkan informasi buku
    public void tampilkanInfoBuku() {
        System.out.println("Judul: " + judul);
        System.out.println("Penulis: " + penulis);
        System.out.println("Tahun Terbit: " + tahunTerbit);
        System.out.println("Status: " + (tersedia ? "Tersedia" : "Tidak Tersedia"));
    }

    // untuk meminjam buku
    public void pinjamBuku() {
        if (tersedia) {
            System.out.println("Buku tersedia & dapat dipinjam.");
            tersedia = false;
        } else {
            System.out.println("Buku tidak tersedia.");
        }
    }

    public static void main(String[] args) {
        Buku buku1 = new Buku("Perjalanan Ais", "Bambang Tutuko", 2023);

        // menampilkan informasi buku sebelum dipinjam
        System.out.println("Informasi buku sebelum dipinjam:");
        buku1.tampilkanInfoBuku();

        // meminjam buku
        buku1.pinjamBuku();

        // menampilkan informasi buku setelah dipinjam
        System.out.println("\nInformasi buku setelah dipinjam:");
        buku1.tampilkanInfoBuku();
    }
}

8. Akun
    public class Akun {
    private String username;
    private String password;
    private boolean aktif;

    // inisialisasi atribut akun
    public Akun(String username, String password) {
        this.username = username;
        this.aktif = false;
    }

    // menampilkan informasi akun
    public void tampilkanInfoAkun() {
        System.out.println("Username: " + username);
        System.out.println("Status: " + (aktif ? "Aktif" : "Nonaktif"));
    }

    // mengaktifkan akun
    public void aktifkanAkun() {
        if (!aktif) {
            System.out.println("Akun berhasil diaktifkan.");
            aktif = true;
        } else {
            System.out.println("Akun sudah aktif.");
        }
    }

    // menonaktifkan akun
    public void nonaktifkanAkun() {
        if (aktif) {
            System.out.println("Akun berhasil dinonaktifkan.");
            aktif = false;
        } else {
            System.out.println("Akun sudah nonaktif.");
        }
    }

    public static void main(String[] args) {
        // membuat objek akun
        Akun akun1 = new Akun("aisyah putri", "choi29");

        // menampilkan informasi akun sebelum diaktifkan
        System.out.println("Informasi akun sebelum diaktifkan:");
        akun1.tampilkanInfoAkun();

        // mengaktifkan akun
        akun1.aktifkanAkun();

        // menampilkan informasi akun setelah diaktifkan
        System.out.println("\nInformasi akun setelah diaktifkan:");
        akun1.tampilkanInfoAkun();

        // menonaktifkan akun
        akun1.nonaktifkanAkun();

        // menampilkan informasi akun setelah dinonaktifkan
        System.out.println("\nInformasi akun setelah dinonaktifkan:");
        akun1.tampilkanInfoAkun();
    }
}

9. Stack
import java.util.Stack;

public class PemeriksaKurung {
    public static boolean isBracketSequenceValid(String expression) {
        Stack<Character> stack = new Stack<>();

        for (char c : expression.toCharArray()) {
            if (c == '(' || c == '[' || c == '{') {
                stack.push(c);
            } else if (c == ')' || c == ']' || c == '}') {
                if (stack.isEmpty()) {
                    return false;
                }

                char top = stack.pop();
                if ((c == ')' && top != '(') || (c == ']' && top != '[') || (c == '}' && top != '{')) {
                    return false;
                }
            }
        }

        return stack.isEmpty();
    }

    /**
     * @param args
     */
    public static void main(String[] args) {
        String expression1 = "((2 + 5) * 3)";
        String expression2 = "((2 + 5) * 3";
        String expression3 = "((2 + 5) * 3))";
        String expression4 = "((2 + 5) * 3]";

        System.out.println(expression1 + " : " + isBracketSequenceValid(expression1));
        System.out.println(expression2 + " : " + isBracketSequenceValid(expression2));
        System.out.println(expression3 + " : " + isBracketSequenceValid(expression3));
        System.out.println(expression4 + " : " + isBracketSequenceValid(expression4));

    }
}

