<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modul 2: HTML Multimedia & API</title>
    <!-- Memuat Tailwind CSS untuk styling -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Style kustom untuk elemen yang tidak di-style bawaan oleh Tailwind */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f3f4f6; /* gray-100 */
            display: flex;
            flex-direction: column;
            min-height: 100vh;
        }
        .content-wrapper {
            flex: 1;
        }
        pre {
            background-color: #f4f4f5; /* zinc-100 */
            padding: 1rem;
            border-radius: 0.5rem; /* rounded-lg */
            overflow-x: auto;
            font-family: 'Courier New', Courier, monospace;
            margin-top: 1rem;
            margin-bottom: 1rem;
        }
        code {
            font-family: 'Courier New', Courier, monospace;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 1.5rem;
            margin-bottom: 1.5rem;
            box-shadow: 0 1px 3px 0 rgba(0, 0, 0, 0.1), 0 1px 2px 0 rgba(0, 0, 0, 0.06);
            border-radius: 0.5rem;
            overflow: hidden;
        }
        th, td {
            border: 1px solid #d4d4d8; /* zinc-300 */
            padding: 0.75rem;
            text-align: left;
            vertical-align: top;
        }
        th {
            background-color: #f4f4f5; /* zinc-100 */
            font-weight: 600;
        }
        tr:nth-child(even) {
            background-color: #fafafa; /* zinc-50 */
        }
        h1 {
            font-size: 2.25rem; /* text-3xl */
            font-weight: 700; /* font-bold */
            margin-bottom: 1rem;
            border-bottom: 2px solid #e4e4e7; /* zinc-200 */
            padding-bottom: 0.5rem;
            color: #18181b; /* zinc-900 */
        }
        h2 {
            font-size: 1.875rem; /* text-2xl */
            font-weight: 600; /* font-semibold */
            margin-top: 2.5rem;
            margin-bottom: 1.5rem;
            color: #27272a; /* zinc-800 */
        }
        h3 {
            font-size: 1.5rem; /* text-xl */
            font-weight: 600; /* font-semibold */
            margin-top: 2rem;
            margin-bottom: 1rem;
            color: #3f3f46; /* zinc-700 */
        }
        p, li {
            margin-bottom: 1rem;
            line-height: 1.6;
            color: #52525b; /* zinc-600 */
        }
        ul {
            list-style-type: disc;
            padding-left: 2rem;
        }
        /* Style untuk tombol pada contoh JS */
        button.example-btn {
            background-color: #0969da;
            color: white;
            padding: 8px 16px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 500;
            margin: 4px;
        }
        button.example-btn:hover {
            background-color: #0a5cc0;
        }
        /* Style untuk footer */
        footer {
            text-align: center;
            padding: 2rem;
            margin-top: 3rem;
            background-color: #e4e4e7; /* zinc-200 */
            color: #52525b; /* zinc-600 */
            font-size: 0.875rem; /* text-sm */
        }
    </style>
</head>
<body class="bg-gray-100 p-4 md:p-8">

    <div class="content-wrapper max-w-5xl mx-auto p-6 md:p-10 bg-white shadow-xl rounded-lg mt-8">

        <h1>MODUL 2. HTML Audio, Video, Youtube dan API</h1>

        <!-- Bagian Dasar Teori -->
        <section>
            <h2>Dasar Teori</h2>
            <p>Multimedia dalam web adalah suara, musik, video, film, dan animasi. Multimedia hadir dalam berbagai format. Multimedia bisa berupa apa saja yang bisa didengar atau dilihat. Contoh: Gambar, musik, suara, video, rekaman, film, animasi, dan banyak lagi.</p>
            <p>Halaman web sering mengandung elemen multimedia dari berbagai jenis dan format.</p>

            <h3>Bentuk (format) Multimedia</h3>
            <p>Elemen multimedia (seperti audio atau video) disimpan dalam file media. Cara yang paling umum untuk menemukan jenis file, adalah dengan melihat ekstensi file. File multimedia memiliki format dan ekstensi berbeda seperti: .swf, .wav, .mp3, .mp4, .mpg, .wmv, and .avi.</p>

            <h3>Bentuk-bentuk video yang umum</h3>
            <p>MP4 adalah format yang baru dan akan datang untuk penggunaan di video internet. MP4 direkomendasikan oleh YouTube, didukung oleh Pemutar Flash, dan didukung oleh HTML5.</p>
            <table>
                <thead>
                    <tr>
                        <th>Format</th>
                        <th>File</th>
                        <th>Description</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>MPEG</td>
                        <td>.mpg .mpeg</td>
                        <td>Dikembangkan oleh Moving Pictures Expert Group. Format video popular yang pertama di web. Tidak didukung dalam HTML5.</td>
                    </tr>
                    <tr>
                        <td>AVI</td>
                        <td>.avi</td>
                        <td>(Audio Video Interleave). Dikembangkan oleh Microsoft. Biasa digunakan dalam kamera video. Tidak di browser web.</td>
                    </tr>
                    <tr>
                        <td>WMV</td>
                        <td>.wmv</td>
                        <td>(Windows Media Video). Dikembangkan oleh Microsoft. Biasa digunakan dalam kamera video. Tidak di browser web.</td>
                    </tr>
                    <tr>
                        <td>QuickTime</td>
                        <td>.mov</td>
                        <td>Dikembangkan oleh Apple. Biasa digunakan dalam kamera video. Tidak di browser.</td>
                    </tr>
                    <tr>
                        <td>RealVideo</td>
                        <td>.rm .ram</td>
                        <td>Dikembangkan oleh Real Media untuk streaming bandwidth rendah. Tidak diputar di browser web.</td>
                    </tr>
                    <tr>
                        <td>Flash</td>
                        <td>.swf .flv</td>
                        <td>Dikembangkan oleh Macromedia. Seringkali membutuhkan plug-in.</td>
                    </tr>
                    <tr>
                        <td>Ogg</td>
                        <td>.ogg</td>
                        <td>Theora Ogg. Dikembangkan oleh the Xiph.Org Foundation. Didukung oleh HTML5.</td>
                    </tr>
                    <tr>
                        <td>WebM</td>
                        <td>.webm</td>
                        <td>Dikembangkan oleh Mozilla, Opera, Adobe, and Google. Didukung oleh HTML5.</td>
                    </tr>
                    <tr>
                        <td>MPEG-4 (MP4)</td>
                        <td>.mp4</td>
                        <td>Dikembangkan oleh the Moving Pictures Expert Group. Berdasarkan QuickTime. Didukung oleh semua browser HTML5. Direkomendasikan oleh YouTube.</td>
                    </tr>
                </tbody>
            </table>
            <p class="font-semibold text-gray-700">Hanya video MP4, WebM, dan Ogg yang didukung oleh standar HTML5.</p>

            <h3>Bentuk-bentuk Audio</h3>
            <p>MP3 adalah format terbaru untuk musik rekaman terkompresi. Istilah MP3 telah menjadi identik dengan musik digital.</p>
            <table>
                <thead>
                    <tr>
                        <th>Format</th>
                        <th>File</th>
                        <th>Description</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>MIDI</td>
                        <td>.mid .midi</td>
                        <td>(Musical Instrument Digital Interface). Main format for all electronic music devices. Tidak berisi suara, tapi nada digital. Tidak di web browser.</td>
                    </tr>
                    <tr>
                        <td>RealAudio</td>
                        <td>.rm .ram</td>
                        <td>Dikembangkan oleh Real Media untuk streaming bandwidth rendah. Tidak di web browser.</td>
                    </tr>
                    <tr>
                        <td>WMA</td>
                        <td>.wma</td>
                        <td>(Windows Media Audio). Dikembangkan oleh Microsoft. Tidak di web browser.</td>
                    </tr>
                    <tr>
                        <td>AAC</td>
                        <td>.aac</td>
                        <td>(Advanced Audio Coding). Dikembangkan oleh Apple as the default format for iTunes. Tidak di web browser.</td>
                    </tr>
                    <tr>
                        <td>WAV</td>
                        <td>.wav</td>
                        <td>Dikembangkan oleh IBM and Microsoft. Didukung oleh HTML5.</td>
                    </tr>
                    <tr>
                        <td>Ogg</td>
                        <td>.ogg</td>
                        <td>Dikembangkan oleh the Xiph.Org Foundation. Didukung oleh HTML5.</td>
                    </tr>
                    <tr>
                        <td>MP3</td>
                        <td>.mp3</td>
                        <td>Bagian suara dari file MPEG. Format paling populer. Kombinasi kompresi bagus dan kualitas tinggi. Didukung oleh semua browser.</td>
                    </tr>
                    <tr>
                        <td>MP4</td>
                        <td>.mp4</td>
                        <td>Format video, tapi bisa juga untuk audio. Didukung oleh semua browser.</td>
                    </tr>
                </tbody>
            </table>
            <p class="font-semibold text-gray-700">Hanya audio MP3, WAV, dan Ogg yang didukung oleh standar HTML5.</p>
        </section>

        <!-- Bagian Audio HTML5 -->
        <section>
            <h2>Audio pada HTML5</h2>
            <p>Sebelum HTML5, file audio hanya dapat diputar di browser menggunakan plug-in (seperti flash). Elemen &lt;audio&gt; HTML5 menentukan standar untuk menyematkan audio di halaman web.</p>
            
            <h3>The HTML &lt;audio&gt; Element</h3>
            <p>Contoh memutar file audio di HTML:</p>
            <pre><code>&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;body&gt;

&lt;audio controls&gt;
  &lt;source src="https://www.w3schools.com/html/horse.ogg" type="audio/ogg"&gt;
  &lt;source src="https://www.w3schools.com/html/horse.mp3" type="audio/mpeg"&gt;
  Your browser does not support the audio element.
&lt;/audio&gt;

&lt;/body&gt;
&lt;/html&gt;</code></pre>
            <p class="mt-4"><strong>Penjelasan:</strong></p>
            <ul>
                <li>Atribut <code>controls</code> menambahkan kontrol audio, seperti play, pause, dan volume.</li>
                <li>Elemen <code>&lt;source&gt;</code> memungkinkan Anda menentukan file audio alternatif yang dapat dipilih browser. Browser akan menggunakan format pertama yang dikenali.</li>
                <li>Teks di antara tag <code>&lt;audio&gt;</code> dan <code>&lt;/audio&gt;</code> hanya akan ditampilkan di browser yang tidak mendukung elemen <code>&lt;audio&gt;</code>.</li>
            </ul>

            <h3>HTML Audio - Browser Support</h3>
            <table>
                <thead>
                    <tr>
                        <th>Browser</th>
                        <th>MP3</th>
                        <th>WAV</th>
                        <th>OGG</th>
                    </tr>
                </thead>
                <tbody>
                    <tr><td>Internet Explorer</td><td>YES</td><td>NO</td><td>NO</td></tr>
                    <tr><td>Chrome</td><td>YES</td><td>YES</td><td>YES</td></tr>
                    <tr><td>Firefox</td><td>YES</td><td>YES</td><td>YES</td></tr>
                    <tr><td>Safari</td><td>YES</td><td>YES</td><td>NO</td></tr>
                    <tr><td>Opera</td><td>YES</td><td>YES</td><td>YES</td></tr>
                </tbody>
            </table>

            <h3>HTML Audio - Media Types</h3>
            <table>
                <thead><tr><th>File Format</th><th>Media Type</th></tr></thead>
                <tbody>
                    <tr><td>MP3</td><td>audio/mpeg</td></tr>
                    <tr><td>OGG</td><td>audio/ogg</td></tr>
                    <tr><td>WAV</td><td>audio/wav</td></tr>
                </tbody>
            </table>
        </section>

        <!-- Bagian Video HTML5 -->
        <section>
            <h2>Video pada HTML5</h2>
            <p>Sebelum HTML5, video hanya bisa diputar di browser dengan plug-in (seperti flash). Elemen &lt;video&gt; HTML5 menentukan cara standar untuk menyematkan video di halaman web.</p>

            <h3>HTML Video</h3>
            <p>Contoh menampilkan video di halaman web:</p>
            <pre><code>&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;body&gt;

&lt;video width="400" controls&gt;
  &lt;source src="https://www.w3schools.com/html/mov_bbb.mp4" type="video/mp4"&gt;
  &lt;source src="https://www.w3schools.com/html/mov_bbb.ogg" type="video/ogg"&gt;
  Your browser does not support HTML video.
&lt;/video&gt;

&lt;p&gt;
Video courtesy of
&lt;a href="https://www.bigbuckbunny.org/" target="_blank"&gt;Big Buck Bunny&lt;/a&gt;.
&lt;/p&gt;

&lt;/body&gt;
&lt;/html&gt;</code></pre>
            <p class="mt-4"><strong>Penjelasan:</strong></p>
            <ul>
                <li>Atribut <code>controls</code> menambahkan kontrol video, seperti play, pause, dan volume.</li>
                <li>Sebaiknya selalu sertakan atribut <code>width</code> dan <code>height</code>. Jika tidak diatur, halaman mungkin berkedip saat video dimuat.</li>
                <li>Elemen <code>&lt;source&gt;</code> memungkinkan Anda menentukan file video alternatif. Browser akan menggunakan format pertama yang dikenali.</li>
                <li>Teks di antara tag <code>&lt;video&gt;</code> dan <code>&lt;/video&gt;</code> hanya akan ditampilkan di browser yang tidak mendukung elemen <code>&lt;video&gt;</code>.</li>
            </ul>

            <h3>HTML &lt;video&gt; Autoplay</h3>
            <p>Untuk memulai video secara otomatis, gunakan atribut <code>autoplay</code>. Ganti kode <code>&lt;video ... controls&gt;</code> dengan <code>&lt;video ... autoplay&gt;</code>. (Catatan: Banyak browser modern memblokir autoplay dengan suara, Anda mungkin perlu menambahkan atribut <code>muted</code>). </p>

            <h3>HTML Video - Browser Support</h3>
            <table>
                <thead>
                    <tr>
                        <th>Browser</th>
                        <th>MP4</th>
                        <th>WebM</th>
                        <th>Ogg</th>
                    </tr>
                </thead>
                <tbody>
                    <tr><td>Internet Explorer</td><td>YES</td><td>NO</td><td>NO</td></tr>
                    <tr><td>Chrome</td><td>YES</td><td>YES</td><td>YES</td></tr>
                    <tr><td>Firefox</td><td>YES</td><td>YES</td><td>YES</td></tr>
                    <tr><td>Safari</td><td>YES</td><td>NO</td><td>NO</td></tr>
                    <tr><td>Opera</td><td>YES (from 25)</td><td>YES</td><td>YES</td></tr>
                </tbody>
            </table>
            
            <h3>HTML Video - Methods, Properties, and Events</h3>
            <p>HTML5 mendefinisikan metode DOM, properti, dan event untuk elemen &lt;video&gt;. Ini memungkinkan Anda memuat, memutar, dan menjeda video, serta mengatur durasi dan volume menggunakan JavaScript.</p>
            <p>Contoh menggunakan JavaScript:</p>
            
            <!-- Contoh Video Player dengan JS -->
            <div class="border p-4 rounded-lg bg-gray-50">
                <div style="text-align:center">
                    <button class="example-btn" onclick="playPause()">Play/Pause</button>
                    <button class="example-btn" onclick="makeBig()">Big</button>
                    <button class="example-btn" onclick="makeSmall()">Small</button>
                    <button class="example-btn" onclick="makeNormal()">Normal</button>
                    <br><br>
                    <video id="video1" width="420" class="mx-auto rounded-md shadow-md">
                        <source src="https://www.w3schools.com/html/mov_bbb.mp4" type="video/mp4">
                        <source src="https://www.w3schools.com/html/mov_bbb.ogg" type="video/ogg">
                        Your browser does not support HTML5 video.
                    </video>
                </div>
                <script>
                    var myVideo = document.getElementById("video1");
                    function playPause() {
                        if (myVideo.paused)
                            myVideo.play();
                        else
                            myVideo.pause();
                    }
                    function makeBig() { myVideo.width = 560; }
                    function makeSmall() { myVideo.width = 320; }
                    function makeNormal() { myVideo.width = 420; }
                </script>
                <p class="text-center text-sm mt-2">Video courtesy of <a href="https://www.bigbuckbunny.org/" target="_blank" class="text-blue-600 hover:underline">Big Buck Bunny</a>.</p>
            </div>
            
            <p class="mt-4">Kode untuk contoh di atas:</p>
            <pre><code>&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;body&gt;

&lt;div style="text-align:center"&gt;
  &lt;button onclick="playPause()"&gt;Play/Pause&lt;/button&gt;
  &lt;button onclick="makeBig()"&gt;Big&lt;/button&gt;
  &lt;button onclick="makeSmall()"&gt;Small&lt;/button&gt;
  &lt;button onclick="makeNormal()"&gt;Normal&lt;/button&gt;
  &lt;br&gt;&lt;br&gt;
  &lt;video id="video1" width="420"&gt;
    &lt;source src="mov_bbb.mp4" type="video/mp4"&gt;
    &lt;source src="mov_bbb.ogg" type="video/ogg"&gt;
    Your browser does not support HTML5 video.
  &lt;/video&gt;
&lt;/div&gt;

&lt;script&gt;
var myVideo = document.getElementById("video1");
function playPause() {
  if (myVideo.paused)
    myVideo.play();
  else
    myVideo.pause();
}
function makeBig() { myVideo.width = 560; }
function makeSmall() { myVideo.width = 320; }
function makeNormal() { myVideo.width = 420; }
&lt;/script&gt;

&lt;/body&gt;
&lt;/html&gt;</code></pre>
        </section>
        
        <!-- Bagian YouTube -->
        <section>
            <h2>HTML YouTube Videos</h2>
            <p>Cara termudah untuk memutar video di HTML adalah dengan menggunakan YouTube. Ini menghindari masalah format video.</p>

            <h3>Playing a YouTube Video in HTML</h3>
            <p>Untuk memutar video Anda di halaman web:</p>
            <ol class="list-decimal pl-6 mb-4">
                <li>Upload video ke YouTube.</li>
                <li>Catat id video (misalnya, <code>tgbNymZ7vqY</code>).</li>
                <li>Tentukan elemen <code>&lt;iframe&gt;</code> di halaman web Anda.</li>
                <li>Arahkan atribut <code>src</code> ke URL video (<code>https://www.youtube.com/embed/VIDEO_ID</code>).</li>
                <li>Gunakan atribut <code>width</code> dan <code>height</code> untuk menentukan dimensi pemutar.</li>
            </ol>
            
            <p>Contoh (direkomendasikan menggunakan iFrame):</p>
            <pre><code>&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;body&gt;

&lt;iframe width="420" height="315"
  src="https://www.youtube.com/embed/tgbNymZ7vqY"&gt;
&lt;/iframe&gt;

&lt;/body&gt;
&lt;/html&gt;</code></pre>

            <h3>YouTube Autoplay</h3>
            <p>Tambahkan <code>?autoplay=1</code> ke URL YouTube. (Catatan: Mungkin juga memerlukan <code>&mute=1</code>).</p>
            <pre><code>src="https://www.youtube.com/embed/tgbNymZ7vqY?autoplay=1"</code></pre>

            <h3>YouTube Loop</h3>
            <p>Tambahkan <code>?playlist=VIDEO_ID&loop=1</code> ke URL.</p>
            <pre><code>src="https://www.youtube.com/embed/tgbNymZ7vqY?playlist=tgbNymZ7vqY&loop=1"</code></pre>
            
            <h3>YouTube Controls</h3>
            <p>Tambahkan <code>?controls=0</code> untuk menyembunyikan kontrol pemutar.</p>
            <pre><code>src="https://www.youtube.com/embed/tgbNymZ7vqY?controls=0"</code></pre>
        </section>

        <!-- Bagian Geolocation API -->
        <section>
            <h2>HTML Geolocation API</h2>
            <p>HTML Geolocation API digunakan untuk mendapatkan posisi geografis pengguna. Karena ini dapat membahayakan privasi, posisi tidak tersedia kecuali pengguna menyetujuinya.</p>
            <p>Metode <code>getCurrentPosition()</code> digunakan untuk mengembalikan posisi pengguna. Contoh di bawah ini mengembalikan lintang dan bujur posisi pengguna:</p>
            
            <!-- Contoh Geolocation -->
            <div class="border p-4 rounded-lg bg-gray-50">
                <p>Click the button to get your coordinates.</p>
                <button class="example-btn" onclick="getLocation()">Try It</button>
                <p id="demo" class="mt-2 font-medium text-gray-700"></p>
                <script>
                    var geoDemoElement = document.getElementById("demo"); 
                    
                    function getLocation() {
                        if (navigator.geolocation) {
                            navigator.geolocation.getCurrentPosition(showPosition, showError);
                        } else {
                            geoDemoElement.innerHTML = "Geolocation is not supported by this browser.";
                        }
                    }
                    function showPosition(position) {
                        geoDemoElement.innerHTML = "Latitude: " + position.coords.latitude +
                            "<br>Longitude: " + position.coords.longitude;
                    }
                    function showError(error) {
                         switch(error.code) {
                            case error.PERMISSION_DENIED:
                                geoDemoElement.innerHTML = "User denied the request for Geolocation."
                                break;
                            case error.POSITION_UNAVAILABLE:
                                geoDemoElement.innerHTML = "Location information is unavailable."
                                break;
                            case error.TIMEOUT:
                                geoDemoElement.innerHTML = "The request to get user location timed out."
                                break;
                            case error.UNKNOWN_ERROR:
                                geoDemoElement.innerHTML = "An unknown error occurred."
                                break;
                        }
                    }
                </script>
            </div>
            
            <p class="mt-4">Kode untuk contoh di atas:</p>
            <pre><code>&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;body&gt;

&lt;p&gt;Click the button to get your coordinates.&lt;/p&gt;
&lt;button onclick="getLocation()"&gt;Try It&lt;/button&gt;
&lt;p id="demo"&gt;&lt;/p&gt;

&lt;script&gt;
var geoDemoElement = document.getElementById("demo");

function getLocation() {
  if (navigator.geolocation) {
    navigator.geolocation.getCurrentPosition(showPosition);
  } else {
    geoDemoElement.innerHTML = "Geolocation is not supported by this browser.";
  }
}
function showPosition(position) {
  geoDemoElement.innerHTML = "Latitude: " + position.coords.latitude +
  "&lt;br&gt;Longitude: " + position.coords.longitude;
}
&lt;/script&gt;

&lt;/body&gt;
&lt;/html&gt;</code></pre>

            <h3>The getCurrentPosition() Method - Return Data</h3>
            <table>
                <thead>
                    <tr><th>Property</th><th>Returns</th></tr>
                </thead>
                <tbody>
                    <tr><td>coords.latitude</td><td>Garis lintang sebagai angka desimal (selalu dikembalikan)</td></tr>
                    <tr><td>coords.longitude</td><td>Garis bujur sebagai angka desimal (selalu dikembalikan)</td></tr>
                    <tr><td>coords.accuracy</td><td>Akurasi posisi (selalu dikembalikan)</td></tr>
                    <tr><td>coords.altitude</td><td>Ketinggian dalam meter di atas permukaan laut (dikembalikan jika tersedia)</td></tr>
                    <tr><td>coords.altitudeAccuracy</td><td>Akurasi ketinggian posisi (dikembalikan jika tersedia)</td></tr>
                    <tr><td>coords.heading</td><td>Arah sebagai derajat searah jarum jam dari Utara (dikembalikan jika tersedia)</td></tr>
                    <tr><td>coords.speed</td><td>Kecepatan dalam meter per detik (dikembalikan jika tersedia)</td></tr>
                    <tr><td>timestamp</td><td>Tanggal/waktu respons (dikembalikan jika tersedia)</td></tr>
                </tbody>
            </table>
        </section>
        
        <!-- Bagian Drag and Drop API -->
        <section>
            <h2>HTML Drag and Drop API</h2>
            <p>Drag and drop adalah fitur yang sangat umum. Ini adalah saat Anda "mengambil" objek dan "meletakkannya" di lokasi yang berbeda.</p>

            <h3>Make an Element Draggable</h3>
            <p>Pertama-tama: Untuk membuat elemen dapat diseret, atur atribut <code>draggable</code> ke <code>true</code>: <code>&lt;img draggable="true"&gt;</code></p>

            <h3>What to Drag - ondragstart and setData()</h3>
            <p>Tentukan apa yang harus terjadi saat elemen diseret. Atribut <code>ondragstart</code> memanggil fungsi yang menentukan data apa yang akan diseret. Metode <code>dataTransfer.setData()</code> menetapkan tipe data dan nilai data yang diseret.</p>

            <h3>Where to Drop - ondragover</h3>
            <p>Event <code>ondragover</code> menentukan di mana data yang diseret dapat dijatuhkan. Secara default, data/elemen tidak dapat dijatuhkan di elemen lain. Untuk mengizinkan drop, kita harus mencegah penanganan default elemen dengan memanggil <code>event.preventDefault()</code>.</p>

            <h3>Do the Drop - ondrop</h3>
            <p>Saat data yang diseret dijatuhkan, event <code>ondrop</code> terjadi. Panggil <code>preventDefault()</code> untuk mencegah penanganan default browser. Dapatkan data yang diseret dengan <code>dataTransfer.getData()</code>. Tambahkan elemen yang diseret ke elemen drop.</p>

            <!-- Contoh Drag and Drop -->
            <div class="border p-4 rounded-lg bg-gray-50">
                <style>
                    .dropzone {
                        float: left;
                        width: 120px;
                        height: 60px;
                        margin: 10px;
                        padding: 10px;
                        border: 2px dashed #aaaaaa;
                        border-radius: 8px;
                    }
                    #drag1 {
                        cursor: move;
                    }
                </style>
                <h3 class="text-lg font-semibold">Drag and Drop Example</h3>
                <p class="text-sm text-gray-600 mb-2">Drag the W3Schools image between the two boxes.</p>
                <div id="div1" class="dropzone" ondrop="drop(event)" ondragover="allowDrop(event)">
                    <img src="https://www.w3schools.com/html/img_logo.gif" draggable="true" ondragstart="drag(event)" id="drag1" width="88" height="31">
                </div>
                <div id="div2" class="dropzone" ondrop="drop(event)" ondragover="allowDrop(event)"></div>
                <div style="clear:both;"></div>
                <script>
                    function allowDrop(ev) {
                        ev.preventDefault();
                    }
                    function drag(ev) {
                        ev.dataTransfer.setData("text", ev.target.id);
                    }
                    function drop(ev) {
                        ev.preventDefault();
                        var data = ev.dataTransfer.getData("text");
                        // Cek agar drop target adalah div, bukan gambar di dalamnya
                        let target = ev.target;
                        if (target.tagName === "IMG") {
                            target = target.parentNode;
                        }
                        if (target.classList.contains("dropzone")) {
                            target.appendChild(document.getElementById(data));
                        }
                    }
                </script>
            </div>
            
            <p class="mt-4">Kode untuk contoh di atas:</p>
            <pre><code>&lt;!DOCTYPE HTML&gt;
&lt;html&gt;
&lt;head&gt;
&lt;style&gt;
#div1, #div2 {
  float: left;
  width: 100px;
  height: 35px;
  margin: 10px;
  padding: 10px;
  border: 1px solid black;
}
&lt;/style&gt;
&lt;script&gt;
function allowDrop(ev) {
  ev.preventDefault();
}

function drag(ev) {
  ev.dataTransfer.setData("text", ev.target.id);
}

function drop(ev) {
  ev.preventDefault();
  var data = ev.dataTransfer.getData("text");
  ev.target.appendChild(document.getElementById(data));
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;

&lt;h2&gt;Drag and Drop&lt;/h2&gt;
&lt;p&gt;Drag the image back and forth between the two div elements.&lt;/p&gt;

&lt;div id="div1" ondrop="drop(event)" ondragover="allowDrop(event)"&gt;
  &lt;img src="img_w3slogo.gif" draggable="true" ondragstart="drag(event)" id="drag1" width="88" height="31"&gt;
&lt;/div&gt;

&lt;div id="div2" ondrop="drop(event)" ondragover="allowDrop(event)"&gt;&lt;/div&gt;

&lt;/body&gt;
&lt;/html&gt;</code></pre>
        </section>

    </div>

    <!-- FOOTER DIPERBARUI -->
    <footer class="w-full">
        <p>Dibuat oleh:</p>
        <p><strong>Constantio Ariano Isworo</strong> | <strong>220211060136</strong></p>
    </footer>
    <!-- AKHIR FOOTER -->

</body>
</html>

<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modul 2: HTML Multimedia & API</title>
    <!-- Memuat Tailwind CSS untuk styling -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Style kustom untuk elemen yang tidak di-style bawaan oleh Tailwind */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f3f4f6; /* gray-100 */
            display: flex;
            flex-direction: column;
            min-height: 100vh;
        }
        .content-wrapper {
            flex: 1;
        }
        pre {
            background-color: #f4f4f5; /* zinc-100 */
            padding: 1rem;
            border-radius: 0.5rem; /* rounded-lg */
            overflow-x: auto;
            font-family: 'Courier New', Courier, monospace;
            margin-top: 1rem;
            margin-bottom: 1rem;
        }
        code {
            font-family: 'Courier New', Courier, monospace;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 1.5rem;
            margin-bottom: 1.5rem;
            box-shadow: 0 1px 3px 0 rgba(0, 0, 0, 0.1), 0 1px 2px 0 rgba(0, 0, 0, 0.06);
            border-radius: 0.5rem;
            overflow: hidden;
        }
        th, td {
            border: 1px solid #d4d4d8; /* zinc-300 */
            padding: 0.75rem;
            text-align: left;
            vertical-align: top;
        }
        th {
            background-color: #f4f4f5; /* zinc-100 */
            font-weight: 600;
        }
        tr:nth-child(even) {
            background-color: #fafafa; /* zinc-50 */
        }
        h1 {
            font-size: 2.25rem; /* text-3xl */
            font-weight: 700; /* font-bold */
            margin-bottom: 1rem;
            border-bottom: 2px solid #e4e4e7; /* zinc-200 */
            padding-bottom: 0.5rem;
            color: #18181b; /* zinc-900 */
        }
        h2 {
            font-size: 1.875rem; /* text-2xl */
            font-weight: 600; /* font-semibold */
            margin-top: 2.5rem;
            margin-bottom: 1.5rem;
            color: #27272a; /* zinc-800 */
        }
        h3 {
            font-size: 1.5rem; /* text-xl */
            font-weight: 600; /* font-semibold */
            margin-top: 2rem;
            margin-bottom: 1rem;
            color: #3f3f46; /* zinc-700 */
        }
        p, li {
            margin-bottom: 1rem;
            line-height: 1.6;
            color: #52525b; /* zinc-600 */
        }
        ul {
            list-style-type: disc;
            padding-left: 2rem;
        }
        /* Style untuk tombol pada contoh JS */
        button.example-btn {
            background-color: #0969da;
            color: white;
            padding: 8px 16px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 500;
            margin: 4px;
        }
        button.example-btn:hover {
            background-color: #0a5cc0;
        }
        /* Style untuk footer */
        footer {
            text-align: center;
            padding: 2rem;
            margin-top: 3rem;
            background-color: #e4e4e7; /* zinc-200 */
            color: #52525b; /* zinc-600 */
            font-size: 0.875rem; /* text-sm */
        }
    </style>
</head>
<body class="bg-gray-100 p-4 md:p-8">

    <div class="content-wrapper max-w-5xl mx-auto p-6 md:p-10 bg-white shadow-xl rounded-lg mt-8">

        <h1>MODUL 2. HTML Audio, Video, Youtube dan API</h1>

        <!-- Bagian Dasar Teori -->
        <section>
            <h2>Dasar Teori</h2>
            <p>Multimedia dalam web adalah suara, musik, video, film, dan animasi. Multimedia hadir dalam berbagai format. Multimedia bisa berupa apa saja yang bisa didengar atau dilihat. Contoh: Gambar, musik, suara, video, rekaman, film, animasi, dan banyak lagi.</p>
            <p>Halaman web sering mengandung elemen multimedia dari berbagai jenis dan format.</p>

            <h3>Bentuk (format) Multimedia</h3>
            <p>Elemen multimedia (seperti audio atau video) disimpan dalam file media. Cara yang paling umum untuk menemukan jenis file, adalah dengan melihat ekstensi file. File multimedia memiliki format dan ekstensi berbeda seperti: .swf, .wav, .mp3, .mp4, .mpg, .wmv, and .avi.</p>

            <h3>Bentuk-bentuk video yang umum</h3>
            <p>MP4 adalah format yang baru dan akan datang untuk penggunaan di video internet. MP4 direkomendasikan oleh YouTube, didukung oleh Pemutar Flash, dan didukung oleh HTML5.</p>
            <table>
                <thead>
                    <tr>
                        <th>Format</th>
                        <th>File</th>
                        <th>Description</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>MPEG</td>
                        <td>.mpg .mpeg</td>
                        <td>Dikembangkan oleh Moving Pictures Expert Group. Format video popular yang pertama di web. Tidak didukung dalam HTML5.</td>
                    </tr>
                    <tr>
                        <td>AVI</td>
                        <td>.avi</td>
                        <td>(Audio Video Interleave). Dikembangkan oleh Microsoft. Biasa digunakan dalam kamera video. Tidak di browser web.</td>
                    </tr>
                    <tr>
                        <td>WMV</td>
                        <td>.wmv</td>
                        <td>(Windows Media Video). Dikembangkan oleh Microsoft. Biasa digunakan dalam kamera video. Tidak di browser web.</td>
                    </tr>
                    <tr>
                        <td>QuickTime</td>
                        <td>.mov</td>
                        <td>Dikembangkan oleh Apple. Biasa digunakan dalam kamera video. Tidak di browser.</td>
                    </tr>
                    <tr>
                        <td>RealVideo</td>
                        <td>.rm .ram</td>
                        <td>Dikembangkan oleh Real Media untuk streaming bandwidth rendah. Tidak diputar di browser web.</td>
                    </tr>
                    <tr>
                        <td>Flash</td>
                        <td>.swf .flv</td>
                        <td>Dikembangkan oleh Macromedia. Seringkali membutuhkan plug-in.</td>
                    </tr>
                    <tr>
                        <td>Ogg</td>
                        <td>.ogg</td>
                        <td>Theora Ogg. Dikembangkan oleh the Xiph.Org Foundation. Didukung oleh HTML5.</td>
                    </tr>
                    <tr>
                        <td>WebM</td>
                        <td>.webm</td>
                        <td>Dikembangkan oleh Mozilla, Opera, Adobe, and Google. Didukung oleh HTML5.</td>
                    </tr>
                    <tr>
                        <td>MPEG-4 (MP4)</td>
                        <td>.mp4</td>
                        <td>Dikembangkan oleh the Moving Pictures Expert Group. Berdasarkan QuickTime. Didukung oleh semua browser HTML5. Direkomendasikan oleh YouTube.</td>
                    </tr>
                </tbody>
            </table>
            <p class="font-semibold text-gray-700">Hanya video MP4, WebM, dan Ogg yang didukung oleh standar HTML5.</p>

            <h3>Bentuk-bentuk Audio</h3>
            <p>MP3 adalah format terbaru untuk musik rekaman terkompresi. Istilah MP3 telah menjadi identik dengan musik digital.</p>
            <table>
                <thead>
                    <tr>
                        <th>Format</th>
                        <th>File</th>
                        <th>Description</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>MIDI</td>
                        <td>.mid .midi</td>
                        <td>(Musical Instrument Digital Interface). Main format for all electronic music devices. Tidak berisi suara, tapi nada digital. Tidak di web browser.</td>
                    </tr>
                    <tr>
                        <td>RealAudio</td>
                        <td>.rm .ram</td>
                        <td>Dikembangkan oleh Real Media untuk streaming bandwidth rendah. Tidak di web browser.</td>
                    </tr>
                    <tr>
                        <td>WMA</td>
                        <td>.wma</td>
                        <td>(Windows Media Audio). Dikembangkan oleh Microsoft. Tidak di web browser.</td>
                    </tr>
                    <tr>
                        <td>AAC</td>
                        <td>.aac</td>
                        <td>(Advanced Audio Coding). Dikembangkan oleh Apple as the default format for iTunes. Tidak di web browser.</td>
                    </tr>
                    <tr>
                        <td>WAV</td>
                        <td>.wav</td>
                        <td>Dikembangkan oleh IBM and Microsoft. Didukung oleh HTML5.</td>
                    </tr>
                    <tr>
                        <td>Ogg</td>
                        <td>.ogg</td>
                        <td>Dikembangkan oleh the Xiph.Org Foundation. Didukung oleh HTML5.</td>
                    </tr>
                    <tr>
                        <td>MP3</td>
                        <td>.mp3</td>
                        <td>Bagian suara dari file MPEG. Format paling populer. Kombinasi kompresi bagus dan kualitas tinggi. Didukung oleh semua browser.</td>
                    </tr>
                    <tr>
                        <td>MP4</td>
                        <td>.mp4</td>
                        <td>Format video, tapi bisa juga untuk audio. Didukung oleh semua browser.</td>
                    </tr>
                </tbody>
            </table>
            <p class="font-semibold text-gray-700">Hanya audio MP3, WAV, dan Ogg yang didukung oleh standar HTML5.</p>
        </section>

        <!-- Bagian Audio HTML5 -->
        <section>
            <h2>Audio pada HTML5</h2>
            <p>Sebelum HTML5, file audio hanya dapat diputar di browser menggunakan plug-in (seperti flash). Elemen &lt;audio&gt; HTML5 menentukan standar untuk menyematkan audio di halaman web.</p>
            
            <h3>The HTML &lt;audio&gt; Element</h3>
            <p>Contoh memutar file audio di HTML:</p>
            <pre><code>&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;body&gt;

&lt;audio controls&gt;
  &lt;source src="https://www.w3schools.com/html/horse.ogg" type="audio/ogg"&gt;
  &lt;source src="https://www.w3schools.com/html/horse.mp3" type="audio/mpeg"&gt;
  Your browser does not support the audio element.
&lt;/audio&gt;

&lt;/body&gt;
&lt;/html&gt;</code></pre>
            <p class="mt-4"><strong>Penjelasan:</strong></p>
            <ul>
                <li>Atribut <code>controls</code> menambahkan kontrol audio, seperti play, pause, dan volume.</li>
                <li>Elemen <code>&lt;source&gt;</code> memungkinkan Anda menentukan file audio alternatif yang dapat dipilih browser. Browser akan menggunakan format pertama yang dikenali.</li>
                <li>Teks di antara tag <code>&lt;audio&gt;</code> dan <code>&lt;/audio&gt;</code> hanya akan ditampilkan di browser yang tidak mendukung elemen <code>&lt;audio&gt;</code>.</li>
            </ul>

            <h3>HTML Audio - Browser Support</h3>
            <table>
                <thead>
                    <tr>
                        <th>Browser</th>
                        <th>MP3</th>
                        <th>WAV</th>
                        <th>OGG</th>
                    </tr>
                </thead>
                <tbody>
                    <tr><td>Internet Explorer</td><td>YES</td><td>NO</td><td>NO</td></tr>
                    <tr><td>Chrome</td><td>YES</td><td>YES</td><td>YES</td></tr>
                    <tr><td>Firefox</td><td>YES</td><td>YES</td><td>YES</td></tr>
                    <tr><td>Safari</td><td>YES</td><td>YES</td><td>NO</td></tr>
                    <tr><td>Opera</td><td>YES</td><td>YES</td><td>YES</td></tr>
                </tbody>
            </table>

            <h3>HTML Audio - Media Types</h3>
            <table>
                <thead><tr><th>File Format</th><th>Media Type</th></tr></thead>
                <tbody>
                    <tr><td>MP3</td><td>audio/mpeg</td></tr>
                    <tr><td>OGG</td><td>audio/ogg</td></tr>
                    <tr><td>WAV</td><td>audio/wav</td></tr>
                </tbody>
            </table>
        </section>

        <!-- Bagian Video HTML5 -->
        <section>
            <h2>Video pada HTML5</h2>
            <p>Sebelum HTML5, video hanya bisa diputar di browser dengan plug-in (seperti flash). Elemen &lt;video&gt; HTML5 menentukan cara standar untuk menyematkan video di halaman web.</p>

            <h3>HTML Video</h3>
            <p>Contoh menampilkan video di halaman web:</p>
            <pre><code>&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;body&gt;

&lt;video width="400" controls&gt;
  &lt;source src="https://www.w3schools.com/html/mov_bbb.mp4" type="video/mp4"&gt;
  &lt;source src="https://www.w3schools.com/html/mov_bbb.ogg" type="video/ogg"&gt;
  Your browser does not support HTML video.
&lt;/video&gt;

&lt;p&gt;
Video courtesy of
&lt;a href="https://www.bigbuckbunny.org/" target="_blank"&gt;Big Buck Bunny&lt;/a&gt;.
&lt;/p&gt;

&lt;/body&gt;
&lt;/html&gt;</code></pre>
            <p class="mt-4"><strong>Penjelasan:</strong></p>
            <ul>
                <li>Atribut <code>controls</code> menambahkan kontrol video, seperti play, pause, dan volume.</li>
                <li>Sebaiknya selalu sertakan atribut <code>width</code> dan <code>height</code>. Jika tidak diatur, halaman mungkin berkedip saat video dimuat.</li>
                <li>Elemen <code>&lt;source&gt;</code> memungkinkan Anda menentukan file video alternatif. Browser akan menggunakan format pertama yang dikenali.</li>
                <li>Teks di antara tag <code>&lt;video&gt;</code> dan <code>&lt;/video&gt;</code> hanya akan ditampilkan di browser yang tidak mendukung elemen <code>&lt;video&gt;</code>.</li>
            </ul>

            <h3>HTML &lt;video&gt; Autoplay</h3>
            <p>Untuk memulai video secara otomatis, gunakan atribut <code>autoplay</code>. Ganti kode <code>&lt;video ... controls&gt;</code> dengan <code>&lt;video ... autoplay&gt;</code>. (Catatan: Banyak browser modern memblokir autoplay dengan suara, Anda mungkin perlu menambahkan atribut <code>muted</code>). </p>

            <h3>HTML Video - Browser Support</h3>
            <table>
                <thead>
                    <tr>
                        <th>Browser</th>
                        <th>MP4</th>
                        <th>WebM</th>
                        <th>Ogg</th>
                    </tr>
                </thead>
                <tbody>
                    <tr><td>Internet Explorer</td><td>YES</td><td>NO</td><td>NO</td></tr>
                    <tr><td>Chrome</td><td>YES</td><td>YES</td><td>YES</td></tr>
                    <tr><td>Firefox</td><td>YES</td><td>YES</td><td>YES</td></tr>
                    <tr><td>Safari</td><td>YES</td><td>NO</td><td>NO</td></tr>
                    <tr><td>Opera</td><td>YES (from 25)</td><td>YES</td><td>YES</td></tr>
                </tbody>
            </table>
            
            <h3>HTML Video - Methods, Properties, and Events</h3>
            <p>HTML5 mendefinisikan metode DOM, properti, dan event untuk elemen &lt;video&gt;. Ini memungkinkan Anda memuat, memutar, dan menjeda video, serta mengatur durasi dan volume menggunakan JavaScript.</p>
            <p>Contoh menggunakan JavaScript:</p>
            
            <!-- Contoh Video Player dengan JS -->
            <div class="border p-4 rounded-lg bg-gray-50">
                <div style="text-align:center">
                    <button class="example-btn" onclick="playPause()">Play/Pause</button>
                    <button class="example-btn" onclick="makeBig()">Big</button>
                    <button class="example-btn" onclick="makeSmall()">Small</button>
                    <button class="example-btn" onclick="makeNormal()">Normal</button>
                    <br><br>
                    <video id="video1" width="420" class="mx-auto rounded-md shadow-md">
                        <source src="https://www.w3schools.com/html/mov_bbb.mp4" type="video/mp4">
                        <source src="https://www.w3schools.com/html/mov_bbb.ogg" type="video/ogg">
                        Your browser does not support HTML5 video.
                    </video>
                </div>
                <script>
                    var myVideo = document.getElementById("video1");
                    function playPause() {
                        if (myVideo.paused)
                            myVideo.play();
                        else
                            myVideo.pause();
                    }
                    function makeBig() { myVideo.width = 560; }
                    function makeSmall() { myVideo.width = 320; }
                    function makeNormal() { myVideo.width = 420; }
                </script>
                <p class="text-center text-sm mt-2">Video courtesy of <a href="https://www.bigbuckbunny.org/" target="_blank" class="text-blue-600 hover:underline">Big Buck Bunny</a>.</p>
            </div>
            
            <p class="mt-4">Kode untuk contoh di atas:</p>
            <pre><code>&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;body&gt;

&lt;div style="text-align:center"&gt;
  &lt;button onclick="playPause()"&gt;Play/Pause&lt;/button&gt;
  &lt;button onclick="makeBig()"&gt;Big&lt;/button&gt;
  &lt;button onclick="makeSmall()"&gt;Small&lt;/button&gt;
  &lt;button onclick="makeNormal()"&gt;Normal&lt;/button&gt;
  &lt;br&gt;&lt;br&gt;
  &lt;video id="video1" width="420"&gt;
    &lt;source src="mov_bbb.mp4" type="video/mp4"&gt;
    &lt;source src="mov_bbb.ogg" type="video/ogg"&gt;
    Your browser does not support HTML5 video.
  &lt;/video&gt;
&lt;/div&gt;

&lt;script&gt;
var myVideo = document.getElementById("video1");
function playPause() {
  if (myVideo.paused)
    myVideo.play();
  else
    myVideo.pause();
}
function makeBig() { myVideo.width = 560; }
function makeSmall() { myVideo.width = 320; }
function makeNormal() { myVideo.width = 420; }
&lt;/script&gt;

&lt;/body&gt;
&lt;/html&gt;</code></pre>
        </section>
        
        <!-- Bagian YouTube -->
        <section>
            <h2>HTML YouTube Videos</h2>
            <p>Cara termudah untuk memutar video di HTML adalah dengan menggunakan YouTube. Ini menghindari masalah format video.</p>

            <h3>Playing a YouTube Video in HTML</h3>
            <p>Untuk memutar video Anda di halaman web:</p>
            <ol class="list-decimal pl-6 mb-4">
                <li>Upload video ke YouTube.</li>
                <li>Catat id video (misalnya, <code>tgbNymZ7vqY</code>).</li>
                <li>Tentukan elemen <code>&lt;iframe&gt;</code> di halaman web Anda.</li>
                <li>Arahkan atribut <code>src</code> ke URL video (<code>https://www.youtube.com/embed/VIDEO_ID</code>).</li>
                <li>Gunakan atribut <code>width</code> dan <code>height</code> untuk menentukan dimensi pemutar.</li>
            </ol>
            
            <p>Contoh (direkomendasikan menggunakan iFrame):</p>
            <pre><code>&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;body&gt;

&lt;iframe width="420" height="315"
  src="https://www.youtube.com/embed/tgbNymZ7vqY"&gt;
&lt;/iframe&gt;

&lt;/body&gt;
&lt;/html&gt;</code></pre>

            <h3>YouTube Autoplay</h3>
            <p>Tambahkan <code>?autoplay=1</code> ke URL YouTube. (Catatan: Mungkin juga memerlukan <code>&mute=1</code>).</p>
            <pre><code>src="https://www.youtube.com/embed/tgbNymZ7vqY?autoplay=1"</code></pre>

            <h3>YouTube Loop</h3>
            <p>Tambahkan <code>?playlist=VIDEO_ID&loop=1</code> ke URL.</p>
            <pre><code>src="https://www.youtube.com/embed/tgbNymZ7vqY?playlist=tgbNymZ7vqY&loop=1"</code></pre>
            
            <h3>YouTube Controls</h3>
            <p>Tambahkan <code>?controls=0</code> untuk menyembunyikan kontrol pemutar.</p>
            <pre><code>src="https://www.youtube.com/embed/tgbNymZ7vqY?controls=0"</code></pre>
        </section>

        <!-- Bagian Geolocation API -->
        <section>
            <h2>HTML Geolocation API</h2>
            <p>HTML Geolocation API digunakan untuk mendapatkan posisi geografis pengguna. Karena ini dapat membahayakan privasi, posisi tidak tersedia kecuali pengguna menyetujuinya.</p>
            <p>Metode <code>getCurrentPosition()</code> digunakan untuk mengembalikan posisi pengguna. Contoh di bawah ini mengembalikan lintang dan bujur posisi pengguna:</p>
            
            <!-- Contoh Geolocation -->
            <div class="border p-4 rounded-lg bg-gray-50">
                <p>Click the button to get your coordinates.</p>
                <button class="example-btn" onclick="getLocation()">Try It</button>
                <p id="demo" class="mt-2 font-medium text-gray-700"></p>
                <script>
                    var geoDemoElement = document.getElementById("demo"); 
                    
                    function getLocation() {
                        if (navigator.geolocation) {
                            navigator.geolocation.getCurrentPosition(showPosition, showError);
                        } else {
                            geoDemoElement.innerHTML = "Geolocation is not supported by this browser.";
                        }
                    }
                    function showPosition(position) {
                        geoDemoElement.innerHTML = "Latitude: " + position.coords.latitude +
                            "<br>Longitude: " + position.coords.longitude;
                    }
                    function showError(error) {
                         switch(error.code) {
                            case error.PERMISSION_DENIED:
                                geoDemoElement.innerHTML = "User denied the request for Geolocation."
                                break;
                            case error.POSITION_UNAVAILABLE:
                                geoDemoElement.innerHTML = "Location information is unavailable."
                                break;
                            case error.TIMEOUT:
                                geoDemoElement.innerHTML = "The request to get user location timed out."
                                break;
                            case error.UNKNOWN_ERROR:
                                geoDemoElement.innerHTML = "An unknown error occurred."
                                break;
                        }
                    }
                </script>
            </div>
            
            <p class="mt-4">Kode untuk contoh di atas:</p>
            <pre><code>&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;body&gt;

&lt;p&gt;Click the button to get your coordinates.&lt;/p&gt;
&lt;button onclick="getLocation()"&gt;Try It&lt;/button&gt;
&lt;p id="demo"&gt;&lt;/p&gt;

&lt;script&gt;
var geoDemoElement = document.getElementById("demo");

function getLocation() {
  if (navigator.geolocation) {
    navigator.geolocation.getCurrentPosition(showPosition);
  } else {
    geoDemoElement.innerHTML = "Geolocation is not supported by this browser.";
  }
}
function showPosition(position) {
  geoDemoElement.innerHTML = "Latitude: " + position.coords.latitude +
  "&lt;br&gt;Longitude: " + position.coords.longitude;
}
&lt;/script&gt;

&lt;/body&gt;
&lt;/html&gt;</code></pre>

            <h3>The getCurrentPosition() Method - Return Data</h3>
            <table>
                <thead>
                    <tr><th>Property</th><th>Returns</th></tr>
                </thead>
                <tbody>
                    <tr><td>coords.latitude</td><td>Garis lintang sebagai angka desimal (selalu dikembalikan)</td></tr>
                    <tr><td>coords.longitude</td><td>Garis bujur sebagai angka desimal (selalu dikembalikan)</td></tr>
                    <tr><td>coords.accuracy</td><td>Akurasi posisi (selalu dikembalikan)</td></tr>
                    <tr><td>coords.altitude</td><td>Ketinggian dalam meter di atas permukaan laut (dikembalikan jika tersedia)</td></tr>
                    <tr><td>coords.altitudeAccuracy</td><td>Akurasi ketinggian posisi (dikembalikan jika tersedia)</td></tr>
                    <tr><td>coords.heading</td><td>Arah sebagai derajat searah jarum jam dari Utara (dikembalikan jika tersedia)</td></tr>
                    <tr><td>coords.speed</td><td>Kecepatan dalam meter per detik (dikembalikan jika tersedia)</td></tr>
                    <tr><td>timestamp</td><td>Tanggal/waktu respons (dikembalikan jika tersedia)</td></tr>
                </tbody>
            </table>
        </section>
        
        <!-- Bagian Drag and Drop API -->
        <section>
            <h2>HTML Drag and Drop API</h2>
            <p>Drag and drop adalah fitur yang sangat umum. Ini adalah saat Anda "mengambil" objek dan "meletakkannya" di lokasi yang berbeda.</p>

            <h3>Make an Element Draggable</h3>
            <p>Pertama-tama: Untuk membuat elemen dapat diseret, atur atribut <code>draggable</code> ke <code>true</code>: <code>&lt;img draggable="true"&gt;</code></p>

            <h3>What to Drag - ondragstart and setData()</h3>
            <p>Tentukan apa yang harus terjadi saat elemen diseret. Atribut <code>ondragstart</code> memanggil fungsi yang menentukan data apa yang akan diseret. Metode <code>dataTransfer.setData()</code> menetapkan tipe data dan nilai data yang diseret.</p>

            <h3>Where to Drop - ondragover</h3>
            <p>Event <code>ondragover</code> menentukan di mana data yang diseret dapat dijatuhkan. Secara default, data/elemen tidak dapat dijatuhkan di elemen lain. Untuk mengizinkan drop, kita harus mencegah penanganan default elemen dengan memanggil <code>event.preventDefault()</code>.</p>

            <h3>Do the Drop - ondrop</h3>
            <p>Saat data yang diseret dijatuhkan, event <code>ondrop</code> terjadi. Panggil <code>preventDefault()</code> untuk mencegah penanganan default browser. Dapatkan data yang diseret dengan <code>dataTransfer.getData()</code>. Tambahkan elemen yang diseret ke elemen drop.</p>

            <!-- Contoh Drag and Drop -->
            <div class="border p-4 rounded-lg bg-gray-50">
                <style>
                    .dropzone {
                        float: left;
                        width: 120px;
                        height: 60px;
                        margin: 10px;
                        padding: 10px;
                        border: 2px dashed #aaaaaa;
                        border-radius: 8px;
                    }
                    #drag1 {
                        cursor: move;
                    }
                </style>
                <h3 class="text-lg font-semibold">Drag and Drop Example</h3>
                <p class="text-sm text-gray-600 mb-2">Drag the W3Schools image between the two boxes.</p>
                <div id="div1" class="dropzone" ondrop="drop(event)" ondragover="allowDrop(event)">
                    <img src="https://www.w3schools.com/html/img_logo.gif" draggable="true" ondragstart="drag(event)" id="drag1" width="88" height="31">
                </div>
                <div id="div2" class="dropzone" ondrop="drop(event)" ondragover="allowDrop(event)"></div>
                <div style="clear:both;"></div>
                <script>
                    function allowDrop(ev) {
                        ev.preventDefault();
                    }
                    function drag(ev) {
                        ev.dataTransfer.setData("text", ev.target.id);
                    }
                    function drop(ev) {
                        ev.preventDefault();
                        var data = ev.dataTransfer.getData("text");
                        // Cek agar drop target adalah div, bukan gambar di dalamnya
                        let target = ev.target;
                        if (target.tagName === "IMG") {
                            target = target.parentNode;
                        }
                        if (target.classList.contains("dropzone")) {
                            target.appendChild(document.getElementById(data));
                        }
                    }
                </script>
            </div>
            
            <p class="mt-4">Kode untuk contoh di atas:</p>
            <pre><code>&lt;!DOCTYPE HTML&gt;
&lt;html&gt;
&lt;head&gt;
&lt;style&gt;
#div1, #div2 {
  float: left;
  width: 100px;
  height: 35px;
  margin: 10px;
  padding: 10px;
  border: 1px solid black;
}
&lt;/style&gt;
&lt;script&gt;
function allowDrop(ev) {
  ev.preventDefault();
}

function drag(ev) {
  ev.dataTransfer.setData("text", ev.target.id);
}

function drop(ev) {
  ev.preventDefault();
  var data = ev.dataTransfer.getData("text");
  ev.target.appendChild(document.getElementById(data));
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;

&lt;h2&gt;Drag and Drop&lt;/h2&gt;
&lt;p&gt;Drag the image back and forth between the two div elements.&lt;/p&gt;

&lt;div id="div1" ondrop="drop(event)" ondragover="allowDrop(event)"&gt;
  &lt;img src="img_w3slogo.gif" draggable="true" ondragstart="drag(event)" id="drag1" width="88" height="31"&gt;
&lt;/div&gt;

&lt;div id="div2" ondrop="drop(event)" ondragover="allowDrop(event)"&gt;&lt;/div&gt;

&lt;/body&gt;
&lt;/html&gt;</code></pre>
        </section>

    </div>

    <!-- FOOTER DIPERBARUI -->
    <footer class="w-full">
        <p>Dibuat oleh:</p>
        <p><strong>Constantio Ariano Isworo</strong> | <strong>220211060136</strong></p>
    </footer>
    <!-- AKHIR FOOTER -->

</body>
</html>

