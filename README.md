# TFIDFSearch
PD-2 HW5

Here’s a bilingual README for your project:

---

# README

## English Version

### Overview

This project implements a basic search engine using **TF-IDF (Term Frequency-Inverse Document Frequency)** to retrieve documents based on query strings. The project consists of two parts:

1. **Index Serialization**: Parses input text files, builds a search index, and serializes the index to disk.
2. **Search Engine**: Loads the serialized index and processes user queries to return the top `n` documents matching the query based on TF-IDF scores.

### Features

- **TF-IDF Calculation**: Calculates TF-IDF scores for query terms within documents.
- **Query Support**: Supports boolean `AND` and `OR` queries.
- **Efficient Serialization**: Uses Java’s `Serializable` interface to store and retrieve the index from disk.

### Files

- **BuildIndex.java**: Parses the input text file, builds the search index, and serializes it.
- **TFIDFSearch.java**: Processes user queries, deserializes the index, and returns top matching documents.
- **Indexer.java**: Implements the `Serializable` interface to serialize the index.

### Running the Project

#### Step 1: Build the Index

1. Compile the Java files:
   ```bash
   javac Indexer.java BuildIndex.java
   ```
2. Run the `BuildIndex` to create the serialized index:
   ```bash
   java BuildIndex /path/to/corpusfile.txt
   ```
   This creates a `.ser` file for the input corpus.

#### Step 2: Run the Search Engine

1. Compile the search engine:
   ```bash
   javac TFIDFSearch.java
   ```
2. Execute a search query:
   ```bash
   java TFIDFSearch corpus1 testcase.txt
   ```
   Results will be written to `output.txt`.

### Input and Output Format

- **Input**: Each query in the `testcase.txt` follows this format:
  - First line: Number of results (`n`) to output.
  - Subsequent lines: Queries using `AND` and `OR` for combining terms.
  
- **Output**: The top `n` matching document IDs are written to `output.txt`.

### Challenge

- Ensure that your average execution time for all test cases (0–4) is below 30 seconds for challenge points.

---

## 中文版本

### 概述

此項目實現了一個基於 **TF-IDF (詞頻-逆文檔頻率)** 的基本搜尋引擎。該項目分為兩部分：

1. **索引序列化**：解析輸入的文本文件，建立搜索索引並將其序列化存儲至磁碟。
2. **搜尋引擎**：加載序列化的索引並處理使用者查詢，根據 TF-IDF 分數返回最符合的前 `n` 筆結果。

### 功能

- **TF-IDF 計算**：對於文檔中的查詢詞彙計算 TF-IDF 分數。
- **查詢支援**：支援布林運算的 `AND` 和 `OR` 查詢。
- **高效序列化**：使用 Java 的 `Serializable` 介面將索引存儲並加載至磁碟。

### 文件

- **BuildIndex.java**: 解析輸入的文本文件，建立搜尋索引並序列化存儲。
- **TFIDFSearch.java**: 處理使用者查詢，反序列化索引，並返回最符合的文檔。
- **Indexer.java**: 實現 `Serializable` 介面，用於索引序列化。

### 執行項目

#### 第一步：建立索引

1. 編譯 Java 文件：
   ```bash
   javac Indexer.java BuildIndex.java
   ```
2. 使用 `BuildIndex` 建立序列化索引：
   ```bash
   java BuildIndex /path/to/corpusfile.txt
   ```
   此命令會為輸入的語料文件建立一個 `.ser` 文件。

#### 第二步：運行搜尋引擎

1. 編譯搜尋引擎：
   ```bash
   javac TFIDFSearch.java
   ```
2. 執行查詢：
   ```bash
   java TFIDFSearch corpus1 testcase.txt
   ```
   查詢結果會輸出至 `output.txt`。

### 輸入與輸出格式

- **輸入**：`testcase.txt` 中的每個查詢格式如下：
  - 第一行：輸出結果的數量 `n`。
  - 後續行：使用 `AND` 和 `OR` 來組合詞彙的查詢。

- **輸出**：將最符合查詢的 `n` 個文檔 ID 寫入 `output.txt`。

### 挑戰

- 確保所有測試案例 (0–4) 的平均執行時間低於 30 秒以獲得挑戰點。

--- 

Let me know if you need further adjustments!
