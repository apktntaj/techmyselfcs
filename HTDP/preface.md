# PREFACE

How to Design Program (HTDP) adalah buku yang mengajarkan tentang disiplin dalam membangun program yang baik.

Yand dimaksud baik adalah program yang ditulis tidak dengan mental "tinker until it works". Tapi membangun program dengan pemetaan masalah yang sistematis dan perencanaan yang matang.

## Systematic Program Design

Ada dua konsep yang harus dilakukan dalam systematic program design (SDP). Pertama _design recipe_ kedua adalah _iterative refinement_.

### Design recipe

Design recipe adalah langkah-langkah dalam membangun program yang terstruktur dengan harapan bisa meminimalisir kesalahan yang dibuat.

Langkah-langkah design recipe:

- From problem to data analysis;
- signature, purpose statement, header;
- function examples;
- function template;
- function definitions;
- testing.

Contoh penerapan bila ingin membuat function konversi pdf ke excel.

- From problem to data analysis;
  - Identifikasi informasi yang ingin diambil dari pdf lalu tentukan struktur data apa yang paling tepat.
- signature, purpose statement, header;
  - signature: File -> Excel;
  - purpose statment: Fungsi ini menerima file pdf dan menghasilkan file excel dengan bentuk kolom yang telah ditentukan;
  - header: function pdfToExcel(name: File): File {}
- function examples;

```typescript
function pdfToExcel(name: File): File {
  // 1. Baca file PDF
  // 2. Ekstraksi data dari PDF
  // 3. Format data ke model kolom 1
  // 4. Format data ke model kolom 2
  // 5. Format data ke model kolom 3
  // 6. Simpan data ke file Excel
}
```

- function template;

```typescript
const pdfParse = require("pdf-parse");
const XLSX = require("xlsx");

function convertPDFtoExcel(pdfFile) {
  // 1. Baca file PDF
  pdfParse(pdfFile).then((data) => {
    // 2. Ekstraksi data dari PDF
    const extractedData = extractDataFromPDF(data.text);

    // 3. Format data ke model kolom 1
    const model1Data = formatToModel1(extractedData);

    // 4. Format data ke model kolom 2
    const model2Data = formatToModel2(extractedData);

    // 5. Format data ke model kolom 3
    const model3Data = formatToModel3(extractedData);

    // 6. Simpan data ke file Excel
    saveToExcel("model1.xlsx", model1Data);
    saveToExcel("model2.xlsx", model2Data);
    saveToExcel("model3.xlsx", model3Data);
  });
}
```

- function definitions;
- testing.

### Iteartive refinement

Prinsipnya adalah yang penting _works_ dahulu. Baru setelah itu dilakukan _iterative refinement_ dengan memeriksa ulang apakah ada detail yang terlewat atau apakah ada yang bisa diimprove dari kode sebelumnya.

## DrRacket and Teaching Language

Di buku htdp, penulis menggunakan Beginning Student Language (BSL) dan DrRacket sebagai text editor karena alasan kesederhanaannya.

Dibanyak bahasa yang populer terkadang programmer pemula dihadapkan pada masalah kerumitan dalam membaca error. Padahal yang dibutuhkan seorang pemula hanya melatih logika dengan membuat program sederhana. Tapi bahasa yang populer memang dibuat untuk _real world problem_, jadi wajar dalam bahasa itu banyak fitur yang tersemat, termasuk error.

Begitu juga dengan DrRacket.

## Skills that Transfer

Persiapan yang matang adalah separuh kemenangan.

Demikian juga dengan belajar mendesain program secara sistematis, skill ini bisa memberikan keterampilan analitis dan kreatif yang dapat diterapkan di berbagai bidang profesi dan kehidupan sehari-hari.

## This Book and Its Part

## The Differeces
