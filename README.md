# py_git

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
