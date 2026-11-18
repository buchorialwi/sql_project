# Assigment day 18, specialized sql techniques

## The report 
![sql code](the_report_image.png)
![answer](answer_the_report.png)
<br>
**pejelasan**:
pertama kita lakukan join dengan syarat mark studen diantara min_mark dan max_mark. kemudian tampilkan nama yang dapat >=8. setelah itu 
urutkan grade paling tinggi, nama dari alphabert, dan mark terkecil
<br>
<br>
## wheather observasion station 18
![sql code](wheather_observasion_code.png)
![answer](wheather_observasion_answer.png)
<br>
**pejelasan**:
kurangkan nilai latitude_n terbanyak dan terendah begitu juga dengan longitude_n, kemudia ubah tipe data menjadi decimal(10,4)
<br>
<br>
## Top Competitors
![sql code](top_competitors_code.png)
![answer](top_competitors_answer.png)
<br>
**pejelasan**:
gabungkan semua table berdasarkan menggunakan foreign key yang tersedia, kemudian filter yang jawabannya benar benar selesai menggunakan
WHERE s.score = d.score, buat group masing masing individu kemudian filter untuk hacker yang menyelesaikan lebih dari satu kompetisi. setelah itu tampilkan id dan nama hacker berdaasrkan id_challange tertinggi dan nama alphabert.
<br>
<br>
## Ollivander's Inventory
![sql code](Ollivander's_Inventory_code.png)
![answer](Ollivander's_Inventory_answer.png)
<br>
**pejelasan**:
gabungkan table wand dan wand property kemudian filter untuk mencari tongkat non evil dan buat sub query untuk mencari harga termurah dengan cara menggabungkan table sepeti sebelum nya namun filter umur dan power yang sama serta non-evil.
cara kerja sql yaitu dengan dengan mengabil data kemudian di simpan di ram. setelah itu data di evaluasi satu per satu misal di query utama menampilkan 
wand = 121, 200, 1000, 90 
wand_property = 200, 10 ,0
setelah kita mendapati row 1 non-evil kemudian sub-query di jalankan dengan cara kerja yang sama namun hanya menampilkan power dan umur yang sama dengan main query serta non-evil. setelah mendapati row yang setara kemudian cari harga termurah lalu kemudian bandingkan apakahan row 1 main query = harga termurah, jika iya tampilkan data jika tidak maka data tidak di tampilkan. kemudian tampilkan wand dengan umur dan power tertinggi.
<br>
<br>
## Contest Leaderboard
![sql code](Contest_Leaderboard_code.png)
![answer](Contest_Leaderboard_answer.png)
<br>
**pejelasan**:
buat cte assigment kemudian gabungkan tabel hacker dan submission. kemudian filter data yang mana score 0 akan langsung di hapus. tampilkan challange_id, hacker_id, score dan buat row_number untuk membuat peringkat masing masing hacker_id dan setiap challange berdasarkan score 
tertinggi. setelah itu buat main query dari cte assigment yang dimana hanya peringkat 1 yang ditampilkan. setelah itu group by berdasarkan hacker_id kemudian jumlahkan kemudian urutkan berdasarkan score tertinggi dan jika sama maka urutkan hacker_id asc
