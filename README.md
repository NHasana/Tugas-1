# Tugas-1

// 1. menghitung luas persegi panjang
 
#include <iostream>
using namespace std;

int main() {
    // Deklarasi variabel panjang dan lebar
    int length = 5;
    int width = 3;

    // Menghitung luas persegi panjang
    int area = length * width;

    // Menampilkan hasil
    cout << "Luas persegi panjang: " << area << endl;

    return 0;
}

output
luas persegi panjang: 15

// 2. menghitung diameter dan luas lingkaran
#include <iostream>
#include <cmath> // Untuk konstanta M_PI

using namespace std;

int main() {
    // Deklarasi variabel jari-jari
    double radius = 5;

    // Menghitung diameter, keliling, dan luas lingkaran
    double diameter = 2 * radius;
    double circumference = 2 * M_PI * radius;
    double area = M_PI * radius * radius;

    // Menampilkan hasil
    cout << "Diameter: " << diameter << endl;
    cout << "Keliling: " << circumference << endl;
    cout << "Luas: " << area << endl;
    return 0;
}

output
Diameter: 10
Keliling: 31.4159
Luas: 78.539

// 3. menghitung sudut ketiga dari sebuah segitiga jika dua sudut diberikan

#include <iostream>
using namespace std;

int main() {
    // Deklarasi variabel untuk dua sudut yang diberikan
    int angle1 = 80;
    int angle2 = 65;

    // Menghitung sudut ketiga
    int angle3 = 180 - (angle1 + angle2);

    // Menampilkan hasil
    cout << "Sudut ketiga: " << angle3 << " derajat" << endl;

    return 0;
}

output
sudut ketiga: 35 derajat

// 4. menghitung selisih antara dua tanggal dalam satuan hari:
#include <iostream>
#include <ctime>

using namespace std;

int main() {
    // Mendefinisikan tanggal dalam format YYYY, MM, DD
    struct tm date1 = {0, 0, 0, 19, 2, 2024 - 1900}; // 2024-03-19
    struct tm date2 = {0, 0, 0, 21, 2, 2024 - 1900}; // 2024-03-21

    // Mengonversi ke time_t (waktu dalam detik sejak epoch)
    time_t time1 = mktime(&date1);
    time_t time2 = mktime(&date2);

    // Menghitung perbedaan dalam hari
    double difference = difftime(time2, time1) / (60 * 60 * 24);

    // Menampilkan hasil
    cout << "Selisih hari antara kedua tanggal adalah: " << difference << " hari" << endl;

    return 0;
}
output
Selisih hari antara kedua tanggal adalah: 2 hari

// 5. #include <iostream>
#include <sstream>

using namespace std;

int main() {
    string name, word, initials = "";
    
    // Input nama
    cout << "Masukkan nama: ";
    getline(cin, name);

    // Menggunakan stringstream untuk memisahkan kata
    stringstream ss(name);
    while (ss >> word) {
        initials += toupper(word[0]); // Ambil huruf pertama dari setiap kata dan ubah ke huruf besar
    }

    // Menampilkan hasil
    cout << "Inisial: " << initials << endl;

    return 0;
}


#include <iostream>
#include <sstream>

using namespace std;

int main() {
    string name, word, initials = "";
    
    // Input nama
    cout << "Masukkan nama: ";
    getline(cin, name);

    // Menggunakan stringstream untuk memisahkan kata
    stringstream ss(name);
    while (ss >> word) {
        initials += toupper(word[0]); // Ambil huruf pertama dari setiap kata dan ubah ke huruf besar
    }

    // Menampilkan hasil
    cout << "Inisial: " << initials << endl;

    return 0;
}

input
masukan nama: John Doe

output
inisoal: JD

