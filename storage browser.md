JSON.parse() Fungsi tersebut berguna untuk mengonversi sebuah JSON 
yang ditulis dalam bentuk string ke bentuk JSON "asli".

STORAGE WEB ADA 2
=> localStorage
=> sessionStorage

PERBEDAAN :
  localStorage
        => data tidak hilang meskipun browser ditutup
        => data tidak hilang meskipun refresh
        => data hilang jika datanya dihapus
  sessionStorage
        => data hilang saat browser ditutup
        => data tidak hilang saat refresh
        => data hilang jika datanya dihapus

BERBENTUK JSON (object)

METHOD LOCALSTORAGE:
    menyimpan data => localStorage.setItem( key, value );
    mengakses data => localStorage.getItem( key );
    menghapus data => localStorage.removeItem( key );

METHOD SESSIONSTORAGE:
    menyimpan data => sessionStorage.setItem( key, value );
    mengakses data => sessionStorage.getItem( key );
    menghapus data => sessionStorage.removeItem( key );

template: 

// apakah browser support storage atau tidak
window.addEventListener('load', function () {
  if (typeof Storage !== 'undefined') {
        
        // mengecek item di storage sudah dibuat atau belum
        // jika belum maka akan dibuat

        if(localStorage.getItem(namaItem) === null){
                localStorage.setItem(namaItem, value)
        }
        
        if(sessionStorage.getItem(namaItem) === null){
                sessionStorage.setItem(namaItem, value)
        }

  } else {
    alert('Browser yang Anda gunakan tidak mendukung Web Storage');
  }
});


template kedua 

function checkForStorage(){
    // akan return true jika support storage 
    return typeof Storage !== 'undefined';
}