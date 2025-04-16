Py_Git

A Python-based reimplementation of Git's core functionality, built from scratch for educational purposes. This project mimics Git's internals including object storage, trees, commits, branching, tagging, and repository management — using only the Python standard library.

---

## Features

- `init` – Initialize a new Git repository.
- `add` – Stage files in the index.
- `commit` – Commit staged changes with metadata and messages.
- `cat-file` – Inspect raw Git objects.
- `hash-object` – Hash files and optionally store them as Git objects.
- `log` – Visualize commit history (Graphviz-compatible).
- `ls-tree` – Pretty-print a tree object.
- `ls-files` – Show indexed files.
- `checkout` – Restore tree contents into a directory.
- `status` – Show the working directory state.
- `tag` – Create and list lightweight and annotated tags.
- `rev-parse` – Resolve names to hashes (branches, tags, HEAD, etc.).
- `rm` – Remove files from the index and working directory.
- `show-ref` – List references (branches and tags).
- `check-ignore` – Test if paths are ignored.

---

## Getting Started

### Prerequisites

- Python 3.8+
- No third-party libraries required — only the Python standard library.

---

### Initialize a repository

```bash
python3 wyag.py init my-repo
cd my-repo
```

---

### Add & commit a file

```bash
echo "Hello, git-like world!" > hello.txt
python3 ../wyag.py add hello.txt
python3 ../wyag.py commit -m "Initial commit"
```

---

###  Inspect Git-like objects

```bash
python3 ../wyag.py log
python3 ../wyag.py cat-file blob <SHA>
python3 ../wyag.py ls-files --verbose
```

---

### Tags & References

```bash
python3 ../wyag.py tag v1.0
python3 ../wyag.py show-ref
```

---

### Check Tree Structures

```bash
python3 ../wyag.py ls-tree HEAD
python3 ../wyag.py checkout HEAD temp_folder/
```

---

### Debug & Inspect Internals

```bash
python3 ../wyag.py rev-parse HEAD
python3 ../wyag.py check-ignore somefile.txt
python3 ../wyag.py status
```

---

## Example: Visualize Git Log Graph

```bash
python3 wyag.py log HEAD | dot -Tpng -o log.png
```

> **Requires Graphviz**  
> - macOS: `brew install graphviz`  
> - Ubuntu: `sudo apt install graphviz`

---

## Project Structure

```
.
├── wyag.py             # Main CLI entrypoint
├── .git/               # Created on init
├── hello.txt           # Example file
├── README.md           # You're reading it!
```

---

## Contributing

This is a learning project — feel free to fork, explore, and improve it. Bug reports and suggestions are always welcome!

---

## References

- Original concept: [Write Yourself a Git](https://wyag.thb.lt/)
- Git internals: https://git-scm.com/book/en/v2/Git-Internals-Plumbing-and-Porcelain

---

