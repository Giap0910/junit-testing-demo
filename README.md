# Transaction Analyzer

Đây là project Java nhỏ phục vụ bài tập kiểm thử phần mềm.

## Nội dung chính

- Có **vòng lặp**: `for` trong `TransactionAnalyzer.classifyTransactions()`
- Có **lệnh rẽ nhánh**: `if/else` trong cùng phương thức
- Có 2 nhóm kiểm thử JUnit tách riêng theo yêu cầu bài:
  - Issue 1: bao phủ tất cả **các lệnh**
  - Issue 2: bao phủ tất cả **các đường đi khả thi**

## Ý tưởng chương trình

Chương trình phân loại tối đa **2 giao dịch đầu tiên**:

- `EMPTY`: không có giao dịch
- `NON_NEGATIVE_ONLY`: chỉ có số không âm
- `WITHDRAWAL_ONLY`: chỉ có số âm
- `MIXED`: có cả số âm và không âm

Việc chỉ xét tối đa 2 phần tử giúp số đường đi khả thi hữu hạn và dễ chứng minh khi viết kiểm thử đường đi.

## Chạy chương trình

### Cách 1: dùng javac/java

```bash
javac -d out src/main/java/org/example/*.java
java -cp out org.example.App
```

### Cách 2: dùng Maven

```bash
mvn test
```

## Tạo issue trên GitHub

Mình đã chuẩn bị sẵn nội dung ở thư mục `docs/issues/`.
Sau khi push repo lên GitHub, bạn chỉ cần copy nội dung từng file để tạo 2 issue:

1. `docs/issues/issue-1-statement-coverage.md`
2. `docs/issues/issue-2-path-coverage.md`

## Gợi ý commit

- `feat: add transaction analyzer program`
- `docs: add issue descriptions for statement and path coverage`
- `test: resolve #1 with statement coverage JUnit tests`
- `test: resolve #2 with path coverage JUnit tests`
