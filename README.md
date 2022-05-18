<p align="center">
  <h3 align="center">BookShelfAPI - Submission Back-End Pemula</h3>

  <p align="center">
    API Documentations for Bookshelf.
  </p>
</p>

## Description

Project ini adalah submission Dicoding untuk kelas Belajar Membuat Aplikasi Back-End untuk Pemula. Untuk lulus kelas terdapat submission yang harus dikerjakan.

Berikut adalah beberapa saran agar mendapat nilai maksimal:
 - Proyek Bookshelf API harus memenuhi seluruh pengujian otomatis pada Postman request yang bertanda **Mandatory**. Bila salah satu pengujiannya gagal, maka proyek Anda akan kami tolak,
 - Tambahkan fitur query parameters `?name`, `?reading` dan `?finished` pada route GET /books,
- Menerapkan CORS pada seluruh resource yang ada,
- Menggunakan ESLint dan salah satu style guide agar gaya penulisan kode JavaScript lebih konsisten,

## Tech Stack

- @hapi/hapi
- Eslint
- Nanoid
- Nodemon

## Table of contents

- [Get All Books List](#get-all-books-list)
- [Add New Book](#add-new-book)
- [Get Detail Book](#get-detail-book)
- [Update Book](#update-book)
- [Delete Book](#delete-book)

## Get All Books List

Mendapatkan seluruh daftar buku

- ### URL

  /books

- ### Method

  GET
  
- ### Response

```json
{
    "status": "success",
    "data": {
        "books": [
            {
                "id": "Qbax5Oy7L8WKf74l",
                "name": "Buku A",
                "publisher": "Dicoding Indonesia"
            },
            {
                "id": "1L7ZtDUFeGs7VlEt",
                "name": "Buku B",
                "publisher": "Dicoding Indonesia"
            },
            {
                "id": "K8DZbfI-t3LrY7lD",
                "name": "Buku C",
                "publisher": "Dicoding Indonesia"
            }
        ]
    }
}
```

## Add New Book

Menambahkan Buku

- ### URL

  /books

- ### Method

  POST
  
- ### Headers

  Content-Type : application/json
  
- ### Body

  - name : string
  - year : number
  - author : string
  - summary : string
  - publisher : string
  - pageCount : number
  - readPage : number
  - reading : boolean
 
 - ### Response

```json
{
    "status": "success",
    "message": "Buku berhasil ditambahkan",
    "data": {
        "bookId": "1L7ZtDUFeGs7VlEt"
    }
}
```

## Get Detail Book

Mendapatkan detail informasi buku

- ### URL

  /books/{bookId}

- ### Method

  GET
  
- ### Response

```json
{
    "status": "success",
    "data": {
        "book": {
            "id": "aWZBUW3JN_VBE-9I",
            "name": "Buku A Revisi",
            "year": 2011,
            "author": "Jane Doe",
            "summary": "Lorem Dolor sit Amet",
            "publisher": "Dicoding",
            "pageCount": 200,
            "readPage": 26,
            "finished": false,
            "reading": false,
            "insertedAt": "2021-03-05T06:14:28.930Z",
            "updatedAt": "2021-03-05T06:14:30.718Z"
        }
    }
}
```

## Update Book

Mengubah data buku berdasarkan id melalui route

- ### URL

  /books/{bookId}

- ### Method

  PUT
  
- ### Body

  - name : string
  - year : number
  - author : string
  - summary : string
  - publisher : string
  - pageCount : number
  - readPage : number
  - reading : boolean

 - ### Response
 ```json
{
    "status": "success",
    "message": "Buku berhasil diperbarui"
}
```

## Delete Book

Menghapus data buku berdasarkan id melalui route

- ### URL

  /books/{bookId}

- ### Method

  DELETE
  
 - ### Response
 ```json
{
    "status": "success",
    "message": "Buku berhasil dihapus"
}
```
