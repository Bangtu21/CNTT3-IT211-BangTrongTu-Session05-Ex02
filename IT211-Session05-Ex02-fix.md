IT211-Session05-Ex02-fix
Chức năng				Method	URL		Query Param(nếu có)	Status thành công	Status lỗi (Ví dụ
Lấy danh sách sách			GET	/books		?page=1&limit=10	200 OK			400 Bad Request
Lấy chi thiết một sách			GET	/books/{id}	Không			200 OK			404 Not Found
Thêm sách mới				POST	/books		Không			201 Create		400 Bad Request
Cập nhật toàn bộ thông tin của sách	PUT	/books/{id}	Không			200 OK			404 Not Found
Cập nhật giá sách			PATCH	/books/{id}	Không			200 OK			400 Bad Request
Xóa sách				DELETE	/books/{id}	Không			204 No Contetn		404 Not Found
Tạo thẻ mượn mới			POST	/take		Không			201 Create		400 Bad Request
Trả sách (cập nhật ngày trả)		PATCH	/take/{id}	Không			200 OK			404 Not Found

Demo nhỏ:
Lấy tất cả sách của tác giả Nguyễn Nhật Ánh: 
	+ GET /books?author=”Nguyễn Nhật Ánh”
Tạo thẻ mượn:
	+ POST /loans
	Body:
	{
		“bookId”: “3”,
		“borrowName”: “Bàng Trọng Tú”,
		“borrowDate”: “2026-05-20”
	}

