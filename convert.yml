name: C++ to Excel-compatible CSV

on:
  workflow_dispatch:
  push:
    paths:
      - 'main.cpp'
      - '.github/workflows/convert.yml'

jobs:
  convert:
    runs-on: ubuntu-latest

    steps:
      - name: Ambil source code
        uses: actions/checkout@v4

      - name: Compile C++
        run: g++ main.cpp -o program

      - name: Jalankan program
        run: ./program > hasil.csv

      - name: Upload hasil
        uses: actions/upload-artifact@v4
        with:
          name: hasil-excel
          path: hasil.csv
