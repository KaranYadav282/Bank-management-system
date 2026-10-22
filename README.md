# Bank Management System

Second Year BTech project - **Sri Sri University**

A banking program that demonstrates the four pillars of Object-Oriented Programming
(**Encapsulation, Inheritance, Polymorphism, Abstraction**). It is written in **Java**
(desktop application), **Python** (command line) and **JavaScript** (web page), all with the
same classes and the same rules.

**Classes:** `Account` (abstract) - `SavingsAccount` - `CurrentAccount` - `Bank`

**Features:** create accounts, deposit money, withdraw money, check balances, and import a CSV
file of transactions to see the results.

| Account type | Rule applied in `withdraw()` |
|---|---|
| Savings | the balance must never fall below Rs. 500 |
| Current | the balance may go negative, but not beyond an overdraft of Rs. 10,000 |

## 1. Live web version (opens in Chrome)

The file `index.html` is the complete desktop-style application. Upload your CSV file on the
**CSV Import** tab and the results appear at once. The file is read inside your browser and is
never sent to any server.

**Put it online for free (works 24/7, no payment):**

1. Upload this whole project to a new **public** GitHub repository (for example `Bank-Management-System`).
2. Open the repository, then **Settings -> Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select branch **main** and folder **/ (root)**, then click **Save**.
4. After about one minute your link is ready:

   `https://YOUR-USERNAME.github.io/Bank-Management-System/`

GitHub Pages is free for public repositories and stays online as long as the repository exists.
You can also open `index.html` by double-clicking it.

## 2. Java desktop application

Needs JDK 8 or later (the logo file `logo.png` must be in the folder you run from).

```bash
cd java
javac -d out src/*.java
java -cp out BankApp          # opens the desktop window
java -cp out TestRunner tests.csv   # runs the 12 test cases
```

In the window, open the **CSV Import** tab, click **Choose CSV File...** and select
`data/sample_transactions.csv`.

## 3. Python version

Needs Python 3.8 or later. No extra libraries.

```bash
cd python
python bank_management_system.py ../data/sample_transactions.csv
python bank_management_system.py ../data/sample_transactions.csv -o results.csv
python bank_management_system.py          # interactive menu
```

## CSV format

```
Action,AccountType,HolderName,AccountNumber,Amount
CREATE,SAVINGS,Nishit Modi,,18000
DEPOSIT,,,ACC1001,5000
WITHDRAW,,,ACC1001,4000
BALANCE,,,ACC1001,
```

Actions are `CREATE`, `DEPOSIT`, `WITHDRAW` and `BALANCE`. Accounts are numbered in order of
creation (`ACC1001`, `ACC1002`, ...). The sample file gives **16 rows: 12 successful, 4 rejected,
total balance Rs. 83,000**, in the Java, Python and web versions alike.

## Project structure

```
index.html                  web version (GitHub Pages)
java/src/                   Java source code
java/logo.png               university logo used by the Java window
python/                     Python source code
data/sample_transactions.csv    sample transactions file
data/specification.csv      project specification (features, OOP concepts, classes)
docs/                       project report (Word) and code listing (PDF)
```

## Team

Karan Sanjay Yadav - Ayushman Barik - Nishit Modi - Ashwin Kumar Nayak - Kaushik Shyamal
