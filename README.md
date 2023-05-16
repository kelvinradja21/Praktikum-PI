# Dokumentasi WAIFULIB API
### Anggota Kelompok 
- Muhammad Iqbal Manalu  - 201402011
- Hizkia Winter  - 201402044
- Kelvin Nathanael Lumbanraja  - 201402050
- Muhammad Ridwan Rizki  - 201402059
- Reinhart Dominggo Sahatmartua Lumbantoruan  - 201402077

## 1. Pendahuluan
Waifulib adalah API ramah pengguna yang dirancang untuk memberikan akses ke database / arsip besar yang menyimpan banyak data (identitas) dan gambar dari Waifu [ Waifu mengacu pada karakter fiksi yang umumnya ditemukan di anime atau bentuk media terkait yang disukai oleh seseorang dengan rasa kasih sayang yang sangat mendalam. ].
![Picture1](https://github.com/kelvinradja21/Praktikum-PI/assets/85007577/d39bd650-c229-4afb-867e-17f8849814bc)

## 2. API Base URL
http://127.0.0.1:5000/

## 3. CRUD
CRUD adalah singkatan dari Create, Read, Update, dan Delete. Ini adalah sekumpulan operasi fundamental yang biasa digunakan dalam database dan pengembangan web. 
- CREATE :
Operasi ini melibatkan pembuatan rekaman atau entitas baru dalam database. Hal ini biasanya melibatkan memasukkan data baru ke dalam sistem, seperti menambahkan waifu baru ke dalam database.

| Path          | Request Type  | 
| ------------- |:-------------:| 
| /waifus       | POST          |

- READ :
Operasi ini melibatkan pengambilan atau membaca data yang ada dari database. Hal ini memungkinkan pengguna untuk mengakses dan melihat informasi yang disimpan dalam sistem, seperti mengambil detail dari suatu waifu.

| Path          | Request Type  | 
| ------------- |:-------------:| 
| /waifus       | GET           |
| /waifus/<id>  | GET           |
  
- UPDATE :
Operasi ini melibatkan modifikasi atau pembaruan data yang ada dalam database. Hal ini memungkinkan pengguna untuk membuat perubahan pada informasi yang disimpan dalam sistem, seperti memperbarui data pada waifu.

| Path          | Request Type  | 
| ------------- |:-------------:| 
| /waifus       | PUT           |
  
- DELETE :
Operasi ini melibatkan menghapus atau menghapus data yang ada dari database. Hal ini memungkinkan pengguna untuk menghapus catatan atau entitas tertentu dari sistem, seperti menghapus suatu data waifu pada database.

| Path          | Request Type  | 
| ------------- |:-------------:| 
| /waifus       | DELETE        |
  
## 4. Fields
 
| Name       | Required      | Type    | Behavior       |
| -----------|:-------------:|:-------:|:--------------:|
| id         | YES           | Integer |ID dari waifu yang ingin dicari/diupdate/dihapus oleh pengguna.
| name       | NO            | String  |Name adalah fields yang memuat nama dari waifu pada database.
| description| NO            | String  |Description adalah fields yang memuat deskripsi dari waifu pada database.
  
## 5. Errors
Contoh response JSON pada API error (client side).
 ```
  {
	“message”: “404 Not Found”
  }
 ```
  
 ## 6. Response
 Contoh JSON response pada call /waifus/<id> dengan request type GET
 ```
  {
	“data”: {
	“description”: “Akari Watanabe (渡辺 星, Watanabe Akari) is 	the main female protagonist of the More Than a Married 	Couple, But Not Lovers manga and anime series”,
	“id”:1, 
	“name”: “Akari Watanabe”	
	}
  }
 ```
  
 ## 7. Request
 Contoh request pada call /waifus dengan request type PUT
 ```
  {
    "name": "Akari Watanabe", 
    "description": "Akari Watanabe (渡辺 星, Watanabe Akari) is 	the main female protagonist of the More Than a Married 	Couple, But Not Lovers manga and anime series"
  }
 ```
  
