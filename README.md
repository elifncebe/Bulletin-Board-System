# Bulletin-Board-System
Bulletin Board System (BBS) Project Public
CS200: Sharing Information History

This project is a Python-based simulation of a 1978-era Bulletin Board System (BBS), developed as part of Brown University's CS200 course. It emulates early computing constraints to deepen understanding of resource-limited systems and information-sharing design.

## 🧠 Purpose
The BBS allows users to:
- Connect with a username
- Post public messages (with subject, author, body)
- View summaries or search messages by term
- Read and delete specific messages by ID
- Switch users and disconnect (while preserving messages)

## 💾 Core Features
- **Persistent Storage:** All data saved to file system, not memory
- **Design Constraints:**
  - ≤10 global variables
  - No lists, dicts, or in-memory data structures for messages
  - ≤32 total files, each ≤2048 chars
  - Max 200 active messages
- **REPL Interface:** Command-line based interaction, mimicking original dial-in experience

## 🧩 Functions Implemented
- `connect(username)`
- `post_msg(subj, msg)`
- `print_summary(term)`
- `find_print_msg(id_num)`
- `remove_msg(id_num)`
- `switch_user(username)`
- `disconnect()`
- `clean_reset()`

## 📐 Design Decisions
- Messages stored in files with ID, author, subject, and body on separate lines
- Summary queries implemented using sequential file reads
- Deletion frees space and allows reuse of message IDs

## ✅ Testing
- Implemented test suite (`test_bbs.py`) simulating multi-user sessions
- Validated edge cases: deletion, filtering, switching users, max message limit

## 📊 Performance
- File operation analysis submitted as part of `hw5.pdf`
- Optimization for reduced read/write overhead

## 📍 Takeaways
This project highlights the complexity of building scalable communication tools under extreme resource constraints, echoing challenges in embedded systems and distributed architectures today.
