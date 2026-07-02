# 🐼 Pandas for Auditors — from Excel to code

A hands-on **pandas** course (the Python data-manipulation library) aimed at
**banking auditors** who are comfortable with Excel but not Python specialists.

All data is **fictional and randomly generated** inside the notebooks: you can run
everything and "break" anything without any risk.

---

## 📚 Recommended path

| Step | Notebook | Content |
|---|---|---|
| **1. Course** | [`course/pandas_for_auditors_course.ipynb`](course/pandas_for_auditors_course.ipynb) | Theory and examples: `DataFrame`, read/write, filtering, sorting, `groupby`, `pivot_table`, `merge`, dates, data quality, audit cases, Python lists, and PDF extraction with PyMuPDF. Every concept is mapped to its **Excel equivalent**. |
| **2. Exercises — Beginner** | [`exercises/beginner/`](exercises/beginner/) | First steps on a bank branch's counter operations. |
| **3. Exercises — Intermediate** | [`exercises/intermediate/`](exercises/intermediate/) | Review of a real-estate loan portfolio. |
| **4. Exercises — Advanced** | [`exercises/advanced/`](exercises/advanced/) | AML/CFT audit of financial flows. |
| **5. Exercises — Lists & PDF** | [`exercises/pdf_and_lists/`](exercises/pdf_and_lists/) | Python lists and data extraction from a PDF report. |

> 💡 Work through the course first, then tackle the exercises in order of difficulty.

---

## 🗂️ Repository structure

```
training_junior/
├── README.md
├── course/
│   └── pandas_for_auditors_course.ipynb     # the course (theory + examples)
└── exercises/
    ├── beginner/
    │   ├── exercise_beginner.ipynb           # to complete
    │   └── solution_beginner.ipynb           # answer key
    ├── intermediate/
    │   ├── exercise_intermediate.ipynb
    │   └── solution_intermediate.ipynb
    ├── advanced/
    │   ├── exercise_advanced.ipynb
    │   └── solution_advanced.ipynb
    └── pdf_and_lists/
        ├── exercise_pdf_lists.ipynb
        └── solution_pdf_lists.ipynb
```

For each level:
- the **`exercise_*.ipynb`** notebook holds the prompts and cells to complete (`# Your code here`);
- the **`solution_*.ipynb`** notebook is identical but with the answers.

Always try the exercise **on your own** before opening the solution.

---

## 🎯 The exercise levels

Each level relies on a **different dataset and audit context**.

### 🟢 Beginner — Bank branch counter operations
- **Context**: review of a branch's face-to-face operations (withdrawals, deposits, advisory…).
- **Skills**: `head` / `info` / `describe`, column selection, simple filtering,
  sorting, `value_counts`, single-level `groupby`.

### 🟠 Intermediate — Real-estate loan portfolio
- **Context**: analysis of loan installments, payment delays, and unpaid amounts per branch.
- **Skills**: multi-condition filtering (`&`, `|`, `~`, `.isin()`, `.between()`),
  computed columns (`np.where`, `np.select`), `groupby` + `.agg()`, `pivot_table`,
  data quality (missing values, duplicates).

### 🔵 Advanced — AML/CFT audit of financial flows
- **Context**: compliance / anti-money-laundering — client enrichment, detection of
  atypical behavior, risk scoring.
- **Skills**: `merge` (≈ `VLOOKUP`), time analysis (`.dt`), structuring detection,
  cash flows, high-risk countries, multi-criteria scoring, and Excel export.

### 🟣 Lists & PDF — Extraction from a surveillance report
- **Context**: parsing a quarterly AML/CFT PDF report to rebuild a structured table.
- **Skills**: Python lists (slicing, methods, comprehensions), reading a PDF with
  **PyMuPDF** (`fitz`), extracting dates and countries with regular expressions (`re`),
  and rebuilding a DataFrame.

> ℹ️ The alert criteria (thresholds, country lists…) are **simplified for teaching purposes**
> and do not constitute a real control methodology.

---

## ⚙️ Requirements & installation

You need **Python 3** and a few libraries:

```bash
pip install pandas numpy openpyxl pymupdf jupyter
```

- **pandas** / **numpy**: data manipulation and generation of the demo datasets.
- **openpyxl**: required to read/write Excel files (`read_excel`, `to_excel`).
- **pymupdf**: required for the Lists & PDF exercise (imported as `fitz`).
- **jupyter**: to open and run the notebooks.

### Running the notebooks

```bash
jupyter notebook        # or: jupyter lab
```

Then open the notebook you want and run the cells **in order, top to bottom**
(`Shift` + `Enter`). The first cell of each exercise notebook **generates the data**:
run it before anything else.
