<!-- node:test berperan sebagai test runner yang menawarkan API untuk menuliskan skenario pengujian. -->
<!-- Adapun node:assert berperan sebagai test assertion yang menyediakan objek untuk memvalidasi nilai antara actual (nilai sesungguhnya) dan expected (nilai yang diharapkan). -->

import { describe, it } from 'node:test';
import assert from 'node:assert';
<!-- => describe untuk pembungkus kode testing -->
<!-- => test / it untuk testingnya  -->
<!-- => assert untuk memvalidasi nilai antara actual (nilai sesungguhnya) dan expected (nilai yang diharapkan). -->


//// STUDI KASUS \\\\
misalnya kita memiliki function penjumlahan
>Function add dapat mengoperasikan penjumlahan aritmetika dengan baik.
>Function add membangkitkan error jika nilai argumen dari numA tidak bertipe number.
>Function add membangkitkan error jika nilai argumen dari numB tidak bertipe number.

syntack nya:

describe('latihan', ()=>{
    it('testing pertama', ()>{

        //action

        //pengujian
        const expected = ....;
        assert.equal(hasil, expected)
    })
});



menggunakan bun
Jika Node.js menggunakan assert untuk menguji nilai, Bun menggunakan expect dan matcher. 
=> expect() menerima satu parameter yang menjadi actual value
=> .toBe() sebagai matcher untuk mengujinya dengan expected value. 

=> install 
powershell -c "iwr bun.sh/install.ps1 | iex"

=> verifikasi bun
bun --version

syntack nya seperti berikut:

describe('latihan', ()=>{
    it('testing pertama', ()>{

        code 

        //pengujian

        expect().toBe()
    })
});
