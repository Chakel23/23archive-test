# 23archive-test

<!DOCTYPE html>
<html>
<head>
	<title>Permainan Tebak Tanggal</title>
</head>
<body>
	<h1>Permainan Tebak Tanggal</h1>
	<p>Silakan tebak tanggal jadian kami (Chandadya & Kelvin) serta tanggal ulang tahun kami:</p>

	<!-- Form untuk memasukkan tebakan -->
	<form onsubmit="return cekTebakan()">
		<label>Tanggal Jadian (format: DD-MM)</label>
		<input type="text" id="jadian" placeholder="contoh: 16-05"><br><br>

		<label>Tanggal Ulang Tahun Kelvin (format: DD-MM)</label>
		<input type="text" id="kelvin" placeholder="contoh: 10-02"><br><br>

		<label>Tanggal Ulang Tahun Chandadya (format: DD-MM)</label>
		<input type="text" id="chandadya" placeholder="contoh: 08-12"><br><br>

		<input type="submit" value="Tebak">
	</form>

	<!-- Pesan hasil tebakan -->
	<p id="hasil"></p>

	<script>
		function cekTebakan() {
			// Mendapatkan tebakan dari input form
			var jadian = document.getElementById("jadian").value;
			var kelvin = document.getElementById("kelvin").value;
			var chandadya = document.getElementById("chandadya").value;

			// Memeriksa apakah tebakan benar atau salah
			if (jadian === "16-05" && kelvin === "10-02" && chandadya === "08-12") {
				document.getElementById("hasil").innerHTML = "Selamat, tebakan Anda benar!";
			} else {
				document.getElementById("hasil").innerHTML = "Maaf, tebakan Anda salah. Silakan coba lagi.";
			}

			// Mengembalikan nilai false agar form tidak ter-submit
			return false;
		}
	</script>
</body>
</html>
