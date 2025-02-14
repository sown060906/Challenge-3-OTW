# Challenge-3-OTW
Bandit
level 0
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
có 1 cách khác nữa là 
 khai báo máy chủ và port sau đó khai báo user name 
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
  pwd (print working directory) -> cat /home/bandit1/- hiển thị đường dẫn tuyệt đối sau đó 
	cat < - 

level 2->3 263JGJPfgU6LtdEvgfWU1XP5yac29mFx
tóm tắt level: Tìm mật khẩu trong một file có tên spaces in this filename
	cat "spaces in this filename" cho vào dấu nháy kép để 
	cat spaces\ in\ this\ filename
cần 
level 3->4 MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

	ls-la (liệt kê tất cả mà kể cả các fiel ẩn)

level 4->5 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ

	file ./* (hiện tất các loại file)

level 5->6 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

	find . -size 
	find .  -type f ! -executable -size (tìm trong đường dẫn,file)

level 6->7 HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

	(cd ../.. để ra thư mục gốc) 

	find / -type f -size 33c  -user bandit7 -group bandit6(ko cần chấm tại tìm trên server)
	find / -type f -size 33c  -user bandit7 -group bandit6 2>/dev/null 
	2>/dev/null 2 là đầu ra lỗi đẩy vào dev null 
level 7->8 morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

	cat data.txt | grep millionth 
	
level 8->9 dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc

	cat data.txt|uniq -u thì bỏ hết những thằng giống nhau nếu nó ở cạnh nhau 
	cat data.txt |sort để lọc cno cạnh nhau
	(cat data.txt|sort|uniq -u luôn  hoặc làm ntren r cat data.txt|uniq -u)
	uniq-u thì chỉ để lại tất cả nhưng mấy tk giống nhau chỉ còn 1 duy nhất 
level 9->10 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM

	strings data.txt giúp lấy ký tự kiểu các chuỗi (con người đọc được!?)
	string data.txt | grep == 
level 10->11 FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey

	(đề bài cho base64 luôn)  ở đây có 2 cách dùng tool trên web hoặc syntax 
	của linux  (đặc điểm base64 có dấu = hoặc == ở cuối)
	base64 -d data.txt(-d viết tắt cho decode)
level 11->12 dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

	bài này giống bài trước nhưng là ceasar lùi 13 phát search web ko có syntax
	tax
level 12->13 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
	
	


		
 






