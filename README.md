# CodexBook

CodexBook is an AI-assisted writing platform designed for authors who seek to structure, revise, and expand narrative universes with symbolic depth and textual consistency. Unlike tools that generate stories automatically, CodexBook begins with a human narrative and acts as an editorial orchestrator.

## 🧩 Concept
CodexBook is a symbolic, structured, and AI-assisted authoring system designed to preserve creative intentionality. It positions AI as a tool for deep reflection, not just automation — aiming to empower authors, not replace them.

## 🎯 System Objective
To build a 100% cloud-based web application using Django that allows:
- Book writing organized by chapters
- AI-powered generation, translation, and revision
- Full versioning of every modification
- Export for publishing formats (Kindle, iBooks, etc.)

## 🧠 Architecture Highlights
- **Backend:** Django 5
- **Frontend:** Bootstrap 5 + HTMX
- **Database:** PostgreSQL
- **Media storage:** Cloudinary or S3
- **AI:** OpenAI API (GPT-4.5, Codex CLI, Sora future integration)

## 🧱 Data Model Overview
- `BaseProject`
- `Project`
- `Chapter`
- `ChapterVersion`
- `AISuggestion`
- `TranslationLog`
- `User` (extended auth.User)

## 📦 Metadata Compliance
Includes required metadata for publishing platforms:
- Title, subtitle, impact phrase
- Language, description, category, keywords
- Publisher, edition, ISBN, high-resolution cover

## 🧰 Core Interfaces
- ✍️ Project Editor (metadata, cover, structure)
- 📄 Chapter Editor (side-by-side with AI suggestions)
- 🧙‍♂️ Wizard Book: AI-assisted generation based on author's personal background
- 🈳 Translation module with multilingual sync
- 🕓 Full version history and diff comparisons
- 📤 Export module (PDF, DOCX-ready)

## ✅ Confirmed Functionalities
- Project and chapter CRUD
- Real-time AI feedback
- Manual or Wizard-based book creation
- Translation auditing and synchronization
- Secure export with formatting for digital stores

## 🔁 AI Interaction Flow
- Prompt = original text + author intent + style instructions
- AI responds with refined suggestions
- Author reviews, accepts, rejects, or edits manually
- Full version tracking

## 🔐 Author-Centric Controls
- No automatic overwrites
- Clear logs by user
- Future support for co-authors

## 🌐 Django Application Routes (mvp)
- `/` → Home  
- `/login/`, `/logout/`  
- `/projects/`, `/projects/new/`, `/projects/<id>/edit/`  
- `/chapters/<id>/edit/`, `/projects/<id>/translate/`, `/export/`

## 📍 Author Workflow
1. Create a new project with metadata and cover  
2. Add or generate chapters (manually or with Wizard Book)  
3. Use AI to improve and revise blocks  
4. Track versions and review differences  
5. Translate chapters if needed  
6. Export for publishing platforms

## 🔄 Multilingual Sync
- Each project can have one or more language versions  
- Only updated chapters are reprocessed  
- Translations are auditable and traceable

## 🧠 Use of Sora (planned)
As Sora evolves, CodexBook plans to:
- Simulate narrative reception through distinct agent personas (emotional, analytical, philosophical)  
- Generate symbolic visual feedback to validate tone and atmosphere  
- Offer authors AI-generated multi-modal coherence checks

## 🔗 Related Repositories
This repository connects with an external manuscript repository used for real-world testing:  
🔗 [Manuscript Repository](https://github.com/flavius-pax/a-ordem-pos-quantica-e-a-batuta-de-neris)

## 📅 Next Steps
- Refactor the editing interface to support block-based writing and semantic versioning  
- Finalize styleguide integration for real-time feedback during writing  
- Enable dynamic translation workflows between English and Portuguese with GPT-4.5  
- Prepare CodexBook for first public release under an open source license  
- Integrate external narrative repositories (e.g., the manuscript repo) as modular content sources  
- Begin Sora experimentation phase

## 🔒 License
This project will be released under an open source license soon. It is currently under active development.

---

**📌 Note:** CodexBook is not a book generator. It is an intentional ecosystem where authors orchestrate narrative complexity — and the AI listens, reflects, and serves.

Made with 🧠 by authors, for authors.
