// Mendapatkan elemen HTML yang akan di animasikan
const elem = document.getElementById('elemen');

// Fungsi untuk menganimasikan elemen
function animateElement() {
    let position = 0;
    const interval = setInterval(frame, 10); // Mengatur kecepatan animasi (milidetik)

    function frame() {
        if (position == 100) { // Ketika elemen mencapai posisi akhir
            clearInterval(interval); // Menghentikan animasi
        } else {
            position++; // Menggeser posisi elemen
            elem.style.left = position + 'px'; // Mengubah posisi elemen
        }
    }
}

// Memanggil fungsi untuk memulai animasi
animateElement();
