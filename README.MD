# TUTORIAL 8 - Advance Programming

## Rizqi Bayu Utama - 2206826330

#### How many data your publlsher program will send to the message broker in one run? 
- Jawab: `Publisher` akan mengirim sebanyak 5 data ke message broker dalam sekali run

#### The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?
- Jawab: `Publisher` dan `Subscriber` mengakses ke url yang sama yaitu `amqp://guest:guest@localhost:5672`. Hal ini membuktikan bahwa keduanya saling berkomunikasi dengan message broker yang sama, pesan yang dikirim oleh `Publisher` akan diterima oleh  `Subscriber` yang terhubung ke server.

##### Running RabitMQ
<img src = "static/running.png">

##### Processing Event
Spike terjadi ketika kita melakukan `cargo run` pada `publisher`, hal ini dikarenakan `publisher` mengirimkan data ke message broker dan `subscriber` menerima data tersebut.
<img src = "static/processing event.png">

##### Simulation Slow Subscribers
Saya melakukan `cargo run` berkali-kali sehingga terjadi spike
<img src = "static/slow.png">

##### Monitoring
Saya melakukan `cargo run` dengan adanya jeda kali ini, sehingga spike dapat berkurang dengan cepat
<img src = "static/quicker.png">