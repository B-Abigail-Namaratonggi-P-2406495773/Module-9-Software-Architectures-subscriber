### Reflection

**1. What is AMQP?**

AMQP (Advanced Message Queuing Protocol) adalah protokol standar terbuka (*open standard*) di tingkat aplikasi (*application layer*) yang dirancang khusus untuk *message-oriented middleware*. Secara sederhana, AMQP adalah aturan atau protokol yang mengatur bagaimana pesan (*message*) dikirim, diantrekan (*queuing*), diarahkan (*routing*), dan dijamin keamanannya antar berbagai komponen sistem (seperti *publisher* dan *subscriber*). Pada tutorial ini, protokol inilah yang digunakan oleh RabbitMQ agar layanan kita bisa saling berkomunikasi secara asinkronus dan *reliable*.

**2. What does it mean? `guest:guest@localhost:5672`**

*String* `guest:guest@localhost:5672` adalah sebuah *connection URI* yang digunakan program (baik *publisher* maupun *subscriber*) untuk melakukan autentikasi dan terhubung ke *server* RabbitMQ.
- **first `guest`:** Merupakan *username default* bawaan dari RabbitMQ.
- **second `guest`:** Merupakan *password default* untuk *user* `guest` tersebut.
- **`localhost:5672`:** `localhost` menandakan bahwa *server* RabbitMQ sedang berjalan di mesin/komputer lokal kita sendiri. Sedangkan `5672` adalah *port default* yang dikhususkan oleh RabbitMQ untuk mendengarkan koneksi yang menggunakan protokol AMQP.