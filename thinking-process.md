## Section desk-nav,mobile-nav

แบ่ง `<section>` สองอัน แต่ละอันมี id ที่บอกชัดเจนว่า `desk-nav` กับ `mobile-nav' เพื่อให้เข้าใจว่า แต่ละ section เอาไว้แสดงผลออกมาเป็นยังไง

จากนั้นดูว่าแต่ละอันโชว์/ซ่อนยังไง สังเกตเห็น class แรกของแต่ละอัน

desk-nav = hidden md:flex   (ซ่อนก่อน แต่โชว์เมื่อจอใหญ่)
mobile-nav = flex md:hidden  (โชว์ก่อน แต่ซ่อนเมื่อจอใหญ่)

**md คือขนาดหน้าจอที่มากกว่าหรือเท่ากับ 768 px**

desk-nav ใช้ justify-between เพื่อจัดวางของข้างในให้เป็นขอบซ้ายกับขวา

- ซ้าย: logo + ชื่อ COLMAR ต่อด้วย span ACADEMY  เพื่อทำให้ ACADEMY เป็นสีเทา แยกสองคำออกจากกัน
- ขวา: ul ที่มี flex เพื่อทำให้เมนูเรียงแนวนอน ใช้ ml-4(16 px) เป็น spacing ระหว่าง item ยกเว้น Sign In ที่ใช้ ml-6(24 px)

mobile-nav ใช้รูปภาพแทนเพราะขนาดหน้าเล็กกว่าแบบ desktop 


## Section banner

md:flex บน desktop เพื่อจัด layout แนวนอน, บน mobile ไม่มี flex เลยเป็นแนวตั้งอัตโนมัติ

md:py-8 และ md:pl-6 เพื่อเพิ่ม padding เฉพาะหน้าจอขนาด desktop เท่านั้น ส่วนของ mobile ไม่มี padding ตรงนี้

**div วางของฝั่งซ้าย** ใช้ md:w-3/5 เพื่อให้บน desktop รูปภาพจะใช้พื้นที่ 60% ของ section ทั้งหมด บน mobile กินเต็ม 100% อัตโนมัติ (เพราะไม่ได้ใส่ md:)

**div วางของฝั่งขวา** md:content-center เพื่อไว้สำหรับจัด content ให้อยู่กึ่งกลางแนวตั้งเฉพาะ desktop และ md:pl-6 เอาไว้เพื่อเพิ่ม padding ซ้ายเฉพาะ desktop

# Section info
แบ่งเป็นแบบ desktop และสำหรับหน้าจอโทรศัพท์เหมือนเดิม โดยใช้ hidden md:flex กับ md:hidden
desk-info แบ่ง layout เป็นสองฝั่งด้วย justify-between

div ฝั่งซ้าย w-3/5 สำหรับรูปใหญ่ + หัวข้อ + paragraph
div ฝั่งขวา w-2/5 สำหรับcard 3 อัน เรียงแนวตั้งด้วย flex-col space-y-4 แต่ละ card ใช้ flex items-center จัดรูปซ้าย text ขวา รูปกว้าง w-[35%]

mobile-info ไม่มีรูปใหญ่ฝั่งซ้ายแล้ว แสดงแค่ card 3 อันเรียงแนวตั้ง 

# Section desk-learn / mobile-learn
แบ่งเป็นแบบ desktop และ mobile โดยใช้ md:flex hidden กับ md:hidden

desk-learn ใช้ grid md:grid-cols-3 gap-4 จัด card 6 อันเป็น 3 คอลัมน์ แต่ละ card มีรูป + text ด้านล่าง ใช้ shadow-lg rounded-lg ทำให้ดูเป็น card

mobile-learn ตัดรูปออกทั้งหมด เหลือแค่ชื่อ course เรียงแนวตั้ง ใช้ bg-gray-300 shadow-md แทน card เต็มรูปแบบ