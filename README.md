<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Form Pendaftaran Kelas Memasak</title>
    <!-- Bootstrap CSS -->
    <link href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" rel="stylesheet">
    <!-- Animate.css -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css"/>
    <style>
        .container {
            margin-top: 50px;
        }
        .form-container {
            background-color: #D6A9A3;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(255, 255, 255, 0.1);
            animation: zoomIn 1s ease-out;
        }
        .form-header {
            animation: fadeInDown 1s ease-out;
        }
        .form-group {
            animation: fadeIn 1s ease-out;
        }
        .form-image {
            animation: slideInRight 1s ease-out;
        }
        .btn-block-custom {
            display: block;
            width: 100%;
            text-align: center;
        }
        .btn-image {
            border: none;
            background: transparent;
            cursor: pointer;
        }
        .btn-image img {
            transition: transform 0.3s ease;
        }
        .btn-image img:hover {
            transform: scale(1.1);
        }
        @keyframes zoomIn {
            from {
                transform: scale(0.5);
                opacity: 0;
            }
            to {
                transform: scale(1);
                opacity: 1;
            }
        }
        @keyframes slideInRight {
            from {
                transform: translateX(100%);
                opacity: 0;
            }
            to {
                transform: translateX(0);
                opacity: 1;
            }
        }
        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }
        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-12">
                <div class="row form-container animate__animated animate__zoomIn">
                    <div class="col-md-6">
                        <h2 class="form-header animate__animated animate__fadeInDown">Pendaftaran Kelas Memasak</h2>
                        <form action="/submit_registration" method="post">
                            <div class="form-group animate__animated animate__fadeInLeft">
                                <label for="nama">Nama Lengkap:</label>
                                <input type="text" class="form-control" id="nama" name="nama" aria-label="Nama Lengkap" required>
                            </div>
                            <div class="form-group animate__animated animate__fadeInRight">
                                <label for="tanggal_lahir">Tanggal Lahir:</label>
                                <input type="date" class="form-control" id="tanggal_lahir" name="tanggal_lahir" aria-label="Tanggal Lahir" required>
                            </div>
                            <div class="form-group animate__animated animate__fadeInLeft">
                                <label for="email">Email:</label>
                                <input type="email" class="form-control" id="email" name="email" aria-label="Email Address" required>
                            </div>
                            <div class="form-group animate__animated animate__fadeInRight">
                                <label for="kategori_kelas">Kategori Kelas Memasak yang Ingin Diikuti:</label>
                                <select class="form-control" id="kategori_kelas" name="kategori_kelas" aria-label="Kategori Kelas" required>
                                    <option value="pilih kelas">Pilih Kelas</option>
                                    <option value="reguler">Reguler (Kelas dengan jadwal pertemuan yang tetap dan materi yang terstruktur)</option>
                                    <option value="intensif">Intensif (Kelas dengan durasi lebih singkat namun dengan materi yang padat)</option>
                                    <option value="privat">Privat (Kelas yang diselenggarakan secara privat dengan instruktur pribadi)</option>
                                    <option value="online">Online (Kelas yang dapat diikuti melalui platform online, memungkinkan peserta belajar dari mana saja)</option>
                                    <option value="workshop">Workshop (Kelas singkat yang fokus pada topik atau teknik memasaktertentu)</option> 
                                </select>
                            </div>
                            <div class="form-group animate__animated animate__fadeInLeft">
                                <label>Jenis Kelamin:</label><br>
                                <div class="form-check form-check-inline">
                                    <input class="form-check-input" type="radio" id="pria" name="jenis_kelamin" value="pria" aria-label="Pria" required>
                                    <label class="form-check-label" for="pria">Pria</label>
                                </div>
                                <div class="form-check form-check-inline">
                                    <input class="form-check-input" type="radio" id="wanita" name="jenis_kelamin" value="wanita" aria-label="Wanita">
                                    <label class="form-check-label" for="wanita">Wanita</label>
                                </div>
                            </div>
                            <div class="form-group animate__animated animate__fadeInRight">
                                <label for="alamat">Alamat Tempat Tinggal:</label>
                                <textarea class="form-control" id="alamat" name="alamat" rows="4" aria-label="Alamat Tempat Tinggal" required></textarea>
                            </div>
                            <div class="form-group animate__animated animate__fadeInLeft">
                                <label for="telepon">Nomor Telepon:</label>
                                <input type="text" class="form-control" id="telepon" name="telepon" aria-label="Nomor Telepon" pattern="\d{10}" required>
                            </div>
                            <div class="form-group form-check animate__animated animate__fadeInRight">
                                <input type="checkbox" class="form-check-input" id="setuju" name="setuju" aria-label="Setuju" required>
                                <label class="form-check-label" for="setuju">Saya setuju dengan syarat dan ketentuan</label>
                            </div>
                            <button type="submit" class="btn-image">
                                <img src="ALHAMDULILAH BISAA BROOO ALLAHHU AKBARRR.jpg" alt="Button Image"/>
                            </button>
                        </form>
                    </div>
                    <div class="col-md-6 d-flex align-items-center justify-content-center">
                        <img src="masak.png" alt="Acara Memasak" class="img-fluid form-image animate__animated animate__slideInRight">
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Bootstrap JS and dependencies -->
    <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.5.4/dist/umd/popper.min.js"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>
</body>
</html>
