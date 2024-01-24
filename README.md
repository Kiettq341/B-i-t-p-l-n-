#include <iostream>
#include <cstdlib>
#include <ctime>
#include <string>
#include <random>

using namespace std;

struct NgChoi {
    string tk;
    string mk;
    int tien;
    string sotknganhang;
    string tennganhang; };

void rutTien(NgChoi& ngChoi) {
    string sotknganhang;
    string tennganhang;
    int tienrut;
    cout<<"Nhap so tai khoan ngan hang cua ban: ";
    cin>>sotknganhang;
    cout<<"Nhap ten ngan hang cua ban: ";
    cin>>tennganhang;
    cout<<"Nhap so tien ban muon rut: ";
    cin>>tienrut;
    cout<<"Dang xu li rut tien tu tai khoan "<<ngChoi.sotknganhang<<" tai ngan hang "<<ngChoi.tennganhang<<endl;
    cout<<"Xin vui long cho trong giay lat..." << endl;

    if (tienrut<=ngChoi.tien) {
        ngChoi.tien-=tienrut;
        cout<<"Da rut tien tu tai khoan "<<ngChoi.sotknganhang<<" tai ngan hang "<<ngChoi.tennganhang<<endl;
        cout<<"So tien da rut: " << tienrut<<endl;
        cout<<"So tien con lai trong tai khoan cua ban: "<<ngChoi.tien<<endl; }
        else {
              cout<<"So tien trong vi khong du de rut."<<endl; } }

int main() {
    srand(time(0));
    NgChoi ngChoi;

    cout<<"                                      ";
    cout<<"NHK.BET GAME CA CUOC UY TIN DEN TU CHAU PHI"<<endl;
    cout<<" "<<endl; cout<<" "<<endl;
    cout<<"Tao tai khoan de choi"<<endl;
    cout<<"Nhap ten dang nhap: ";
    cin>>ngChoi.tk;
    cout<<"Nhap mat khau: ";
    cin>>ngChoi.mk;
    cout<<"Ban nen cay ket de co tien nap vao game"<<endl;
    cout<<"Hay nap tien: ";
    cin>>ngChoi.tien;
    cout<<"Tai khoan cua ban da tao thanh cong voi ten "<<ngChoi.tk<<endl;
    cout<<"Neu muon rut tien nhan phim tat '-1'"<<endl;
    cout<<"So tien trong vi cua ban la: "<<ngChoi.tien<<endl;

    while( true){
     int cuoc;
        char chon;

        cout<<"Nhap so tien cuoc: ";
        cin>>cuoc;

        if (cuoc==0) {
            break;
        }

        if (cuoc==-1) {
            rutTien(ngChoi);
            continue; }

        if (cuoc>ngChoi.tien) {
            cout<<"Ban khong du tien cuoc "<<endl;
            continue; }

        cout<<"Ban muon chon chan hay le?? (c/l): ";
        cin>>chon;

        int so=rand()%10;

        cout<<"Con so j day con so j day la con so: "<<so<<endl;

        if ((so%2==0&&chon=='c') || (so%2!=0&&chon=='l')) {
            cout<<"Wowww ban hay qua"<<endl;
            ngChoi.tien+=cuoc; }
            else {
                  cout<<"Chuc ban may man lan sau: "<<cuoc<<endl;
                  ngChoi.tien-=cuoc; }
                  cout<<"So tien trong vi cua ban la: "<<ngChoi.tien<<endl; }
                  cout<<"Cam on ban da tin tuong NHK.BET"<<endl;

    return 0;
}





