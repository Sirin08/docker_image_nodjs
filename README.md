1. ใช้คำสั่ง git clone https://github.com/Sirin08/docker_image_nodjs.git

2.cd เข้าโฟลเดอร์  docker_image_nodjs จากนั้นเปิด code .

3.สร้างfolder เพิ่มเข้ามา ชื่อว่า uploads

4.ใช้คำสั่ง npm install  และใช้คำสั่ง npm install nodemon -g 
*ใช้คำสั่ง npm start แล้วเข้า http://localhost:3333/ เมื่ออัพโหลดรูปภาพ รูปภาพจะถูกเก็บไว้ในโฟลเดอร์ uploads


ต่อ

5.เปิด docker และใช้คำสั่ง docker build -t ponggun/nodeupload . ในterminal vs

*หาก build ไม่ได้ ให้ใช้คำสั่ง npm install และตามด้วยคำสั่ง  docker build -t ponggun/nodeupload . อีกรอบ

6. ใช้คำสั่ง docker run -p 80:3333 -v /home/ponggun/docker_image_nodjs/uploads:/app/uploads ponggun/nodeupload

7.เข้าlinkport ในcontainer  เลือกรูปภาพที่จะอัพโหลด หรือ ใส่link url ของรูปภาพ  แล้วกด upload image
*ในส่วนของตัวนี้ รูปที่อัพโหลดจะไม่เข้าในโฟลเดอร์ uploads ******เนื่องจาก ยังทำไม่ได้ค่ะ******

ปล.หากรูปภาพมีขนาดใหญ่เกิดไปหรือมีลิขสิทธ์ อาจจะทำให้ตัวเว็ปไม่สามารถแสดงโชว์ได้ ขอบคุณค่ะ
