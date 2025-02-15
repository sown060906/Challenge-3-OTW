# Challenge-3-OTW
Em lần đầu dùng github viết writeup ạ, mong anh thông cảm cho em ạ 
 
 Bandit

level 0 bảo chúng ta đăng nhập vào server bằng ssh

	một câu lệnh ssh tối thiểu bao gồm 
 ssh username@host -p port
 
  user name là tên tài khoản 


  host tên server 
  
  -p  là khai báo cổng 
  
  port là mã cổng 
  
	ví dụ như đăng nhập vào bandit0 như sau 

	ssh bandit0@bandit.labs.overthewire.org -p 2220
 ![Screenshot (41)](https://github.com/user-attachments/assets/7c69e74b-ec37-4096-b367-47993c9c4b37)
	có 1 cách khác nữa là khai báo máy chủ và port sau đó khai báo user name 
 
 	ssh host -p port -l username
 
 	ssh bandit.labs.overthewire.org -p2220 -l bandit0 
	

level 0->1 pass: bandit0

  tóm tắt level : Mật khẩu của level tiếp theo nằm trong file readme nằm trong thư mục gốc.
 
 	lệnh ls(list) trong Linux được dùng để liệt kê các tệp và thư mục trong một thư mục.
 	cat readme 
 
 	cat là viết tắt của concatenate trong Linux lệnh này dùng để hiển thị nội dung file
 ![Screenshot (42)](https://github.com/user-attachments/assets/f6aeb163-18e8-44f8-92a8-a3309ad36c95)

level 1->2  ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
	tóm tắt level: Pass nằm trong file tên "-"

	cat ./- dùng đường dẫn tuyệt đối ./file (./ để tránh nhầm lẫn các file có tên bắt đầu từ ký tự đặc biệt)
 ![Screenshot (43)](https://github.com/user-attachments/assets/adf96c63-9403-40e2-b53a-40db567072b7)
	có nhiều cách  
  	pwd (print working directory) -> cat /home/bandit1/- hiển thị đường dẫn tuyệt đối 
  
	cat < - (" < "dùng để chuyển hướng đầu vào  từ một file vào một lệnh trong đây là cat và sử dụng thư mục "-" làm đầu vào)

level 2->3  263JGJPfgU6LtdEvgfWU1XP5yac29mFx
	để chuyển hướng đầu vào (input redirection) từ một file vào một lệnh

	tóm tắt level: Tìm mật khẩu trong một file có tên spaces in this filename

	cat "spaces in this filename" cho vào dấu nháy kép để rõ ràng tên file
 
	cat spaces\ in\ this\ filename (dấu '\ ' để viết ký tự khoảng trắng  
 
![Screenshot (44)](https://github.com/user-attachments/assets/cc2c2e5a-47ce-4864-87ad-aff1d9e201f5)


level 3->4 MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

	tóm tắt level:Tìm mật khẩu trong một file ẩn nằm trong thư mục inhere 
![Screenshot (45)](https://github.com/user-attachments/assets/f0012914-5dec-48af-ab38-8ed62a13ada6)

	cd  (change directory )là lệnh dùng để di chuyển đến các thư mục cách dùng cd filename

	ls-la (liệt kê tất cả mà kể cả các file ẩn)

level 4->5 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ

	tóm tắt level:Tìm mật khẩu trong một file ẩn nằm trong thư mục inhere, chỉ có một file có thể đọc được 

	có 2 cách
 
	cat <  từng file để tìm ra pass 
 ![Screenshot (47)](https://github.com/user-attachments/assets/5c4f2edc-2eb4-4be4-93ae-f40982dcd440)


 
	file ./* (hiện tất dạng loại file của tất cả các file tring thư mục ) vì chỉ có 1 file human readable nên nó sẽ khác dạng với những cái còn lại 
 ![Screenshot (46)](https://github.com/user-attachments/assets/d0c45e4d-168e-4d48-9718-800b5aa3cdee)



level 5->6 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

	tóm tắt level:Tìm mật khẩu trong một file nằm trong thư mục inhere humanreadable 1033 bytes in size
not executable

lệnh find là để tìm các thư mục 

	find . tìm tất cả các thư mục trong thư mục hiện tại


	find . -size 1033c 
 
	find .  -type f ! -executable -size 1033c  (tìm trong đường dẫn,file)
 ![Screenshot (48)](https://github.com/user-attachments/assets/32ae7c56-7aaa-4544-992b-d21bc3e0df6e)


level 6->7 HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

![image](https://github.com/user-attachments/assets/2347c7f0-96d1-4383-bba9-eda8782772c9)



	find / -type f -size 33c  -user bandit7 -group bandit6(ko cần chấm tại tìm trên server)
 
	find / -type f -size 33c  -user bandit7 -group bandit6 2>/dev/null 
 
	2>/dev/null  có nghĩa là : 2 chỉ rằng đầu ra lỗi (không đc quyền truy cập) đẩy vào file dev null 
 ![Screenshot (49)](https://github.com/user-attachments/assets/5e51ec02-5d55-4d52-abec-4ae5bbb1a9c7)

level 7->8 morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
![image](https://github.com/user-attachments/assets/22ddf46c-01fe-4815-8882-85cb9bf79c35)

Dấu | (pipe) được sử dụng để chuyển dữ liệu từ đầu ra của một lệnh làm đầu vào cho lệnh khác.

grep được sử dụng để tìm kiếm chuỗi ký tự trong file hoặc đầu ra của lệnh khác cấu trúc 

	cat data.txt | grep millionth 
 ![Screenshot (50)](https://github.com/user-attachments/assets/a2649f10-a248-4b39-a25f-9fc68496e222)

	
level 8->9 dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
![image](https://github.com/user-attachments/assets/01aa307d-2ff5-414e-b88d-49711dbd83f6)


	
 
	(cat data.txt|sort|uniq -u )
 
 sort để sắp xếp lại các câu giống nhau gần nhau
 
 uniq -u thì bỏ hết những thằng giống nhau nếu chúng ở cạnh nhau 
 
 ![Screenshot (51)](https://github.com/user-attachments/assets/ad19c9eb-536f-480f-898c-d9aeaf2468bf)

level 9->10 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
![image](https://github.com/user-attachments/assets/3e5f2e5e-2d75-4a65-aa9a-80a913bd8bce)


	
	strings data.txt 
 
 	strings data.txt | grep == 

 strings giúp lấy ký tự kiểu các chuỗi (con người đọc được!?)
 ![Screenshot (52)](https://github.com/user-attachments/assets/4a02ed71-fdc5-4e03-afb0-ecc97a662f3a)


level 10->11 FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
![image](https://github.com/user-attachments/assets/dc5092cf-5162-44a5-a7a6-a59df8b0047d)

	(đề bài cho base64 luôn)  ở đây có 2 cách dùng tool trên web hoặc syntax của linux  (đặc điểm base64 có dấu = hoặc == ở cuối)
 
	 syntax  base64 -d data.txt(-d viết tắt cho decode)
level 11->12 dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

	bài này giống bài trước nhưng là ceasar lùi 13 phát search web ko có syntax
	tax
level 12->13 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
	
	


		
 






