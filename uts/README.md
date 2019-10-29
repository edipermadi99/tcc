
# TUGAS UTS TCC
Nama : Edi Permadi  
NIM  : 175410046 

***

1. Mengecek Docker yaitu dengan perintah 

		$ docker -v

2. Membuat folder dengan nama contoh 

    	$ mkdir contoh

3. Masuk ke folder contoh  dan membuat file dengan nama Dockerfile dan mengisi code berikut  

		#image base  
		FROM nginx:alpine  
		#copy aplication file  
		COPY html /usr/share/nginx/html:  

4. Membuat folder html dengan perintah "mkdir html"   
5. Masuk ke folder html dan membuat file index.html dan mengisi kode

		<!DOCTYPE html> 
		<html>
		<body>
		<h1>TUGAS UTS</h1>
		<h2>Nama : Edi Permadi</h2>
		<h2>NIM  : 175410046</h2>
		</body>
		</html>

6. Masuk ke directory dimana file Dockerfile berada, kemudian ketikan perintah berikut untuk build image  
	$ docker build -t aplication:versi-1 .

7. Cek image yang telah terbentuk dengan perintah $ docker images dan akan muncul seperti berikut:  

		REPOSITORY          TAG                 IMAGE ID            CREATED              SIZE  

		aplication          versi-1               b5132100360e        About a minute ago   21.1MB


8. Menjalankan Image dengan perintah  

		$ docker run -d -p 80:80 aplication:versi-1

9. Melihat container yang berjalan yaitu dengan perintah  

		$ docker ps

10. Membuka output melalui browser  

	 ![alt text](img/1.PNG)
