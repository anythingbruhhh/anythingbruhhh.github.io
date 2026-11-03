---
layout: "default"
title: "📄 markdown2pdf-gh-action - Turn Markdown Into PDFs Automatically"
description: "Convert Markdown to PDF in GitHub Actions with iText, producing one PDF or a ZIP of PDFs for folder inputs."
---
# 📄 markdown2pdf-gh-action - Turn Markdown Into PDFs Automatically

[![Download markdown2pdf-gh-action](https://img.shields.io/badge/Download-markdown2pdf--gh--action-ff6b6b?style=for-the-badge&logo=github&logoColor=white)](https://github.com/anythingbruhhh/markdown2pdf-gh-action/releases)

Visit this link to download the application.

## 📌 What This Tool Does

markdown2pdf-gh-action is a GitHub Action that converts Markdown documents into PDF files using iText. It is designed for people who want a repeatable, automated way to turn `.md` files into clean PDF output without manually opening each file.

The action works in two simple ways:

- A **single Markdown file** becomes one `.pdf`.
- A **folder of Markdown files** becomes one `.zip`. Inside the ZIP, each `.md` file has its own PDF. The original folder structure is preserved. The ZIP is created even when the folder contains only one `.md` file.

This is a GitHub Action, so it runs inside GitHub Actions rather than as a desktop Windows program. On Windows, you use your normal web browser to open GitHub, start the action, and collect the finished PDF or ZIP. The conversion itself runs on GitHub’s Ubuntu Linux runner.

## 🪟 Using This on Windows

You do not need to install a separate Windows application to use markdown2pdf-gh-action. You use Windows to open GitHub in a browser, sign in, and run the action from a public repository.

The conversion runs on `ubuntu-latest` Linux x86_64 runners. Self-hosted runners also need Bash, GNU coreutils/findutils, and `zip` on `PATH`.

This action works with **public open source repositories only**. The converter checks repository visibility through the GitHub API and refuses to run when the repository is not public.

## 🚀 Getting Started

1. Visit# 📄 markdown2pdf-gh-action - Turn Markdown Into PDFs Automatically

[![Download markdown2pdf-gh-action](https://img.shields.io/badge/Download-markdown2pdf--gh--action-4c6ef5?style=for-the-badge&logo=github&logoColor=white)](https://github.com/anythingbruhhh/markdown2pdf-gh-action/releases)

Visit this link to download the application.

## 📌 What This Tool Does

markdown2pdf-gh-action is a GitHub Action that converts Markdown documents into PDF files using iText. It gives you a repeatable, automated way to turn `.md` files into clean PDF output without opening and formatting each file by hand.

The action works in two simple ways:

- A **single Markdown file** becomes one `.pdf`.
- A **folder of Markdown files** becomes one `.zip`. Inside the ZIP, every `.md` file gets its own PDF. The original folder structure is preserved. The ZIP is created even when the folder contains only one `.md` file.

The tool produces exactly one output file every time, so you always know what to collect when the run finishes.

## 🪟 Using This on Windows

You do not need to install a desktop Windows program to use markdown2pdf-gh-action. You use Windows to open GitHub in your browser, sign in, and start the action from a public repository. The conversion itself runs on GitHub's servers.

This matters because the action runs on Linux x86_64 runners only (`runs-on: ubuntu-latest`). Self-hosted runners also need Bash, GNU coreutils/findutils, and `zip` on `PATH`. Your Windows PC is simply the place where you view results and download the finished file.

The action works with **public open source repositories only**. The converter checks repository visibility through the GitHub API and refuses to run if the repository is not public.

The converter is already committed to the repository at `bin/itext-markdown2pdf`, so nothing is downloaded at runtime.

## 🚀 Getting Started

1. Visit this link to download the application: **https://github.com/anythingbruhhh/markdown2pdf-gh-action/releases**
2. Sign in to your GitHub account in your browser.
3. Open a public repository where you want to run the conversion.
4. Add your Markdown file, or a folder of Markdown files, to that repository.
5. Create a workflow that uses the markdown2pdf-gh-action step and point it at your file or folder.
6. Start the workflow.
7. When the run finishes, open the run summary and collect the single output file — a `.pdf` or a `.zip`.

If you have never used a GitHub Action before, start with a single file. Once that works, move on to a folder. The steps are the same; only the input changes.

## 💾 Download and Setup

[![Download markdown2pdf-gh-action](https://img.shields.io/badge/Get%20markdown2pdf--gh--action-2f9e44?style=for-the-badge&logo=github&logoColor=white)](https://github.com/anythingbruhhh/markdown2pdf-gh-action/releases)

Visit this link to download the application.

Once you have the repository contents, you have everything needed. There is no installer to run, no separate download step at runtime, and no extra package to fetch. The converter is committed to the repository as `bin/itext-markdown2pdf`.

Because the tool is a GitHub Action, "setup" means preparing a workflow in a public repository. Your workflow needs to:

- Run on `ubuntu-latest`.
- Live in a public repository.
- Pass either a file path or a folder path as the input.
- Collect the single output file when the run completes.

Nothing runs on your Windows machine. Everything runs on GitHub's Ubuntu runner, and your browser is the only tool you need.

## 📥 Inputs

The action accepts one input path at a time. That path decides what you get back.

**File input**

Give the action the path to a single `.md` file. The action converts that document and produces one `.pdf`.

**Folder input**

Give the action the path to a folder. The action scans the folder recursively, finds every `.md` file, and converts each one to its own PDF. All of those PDFs are packed into a single `.zip`, and the input folder structure is preserved inside the archive.

A folder always produces a `.zip`, even when it contains only one Markdown file. This keeps the output predictable: folder in, ZIP out.

## 📤 Outputs

There is always exactly one output file.

- **File input → one `.pdf`.** Download it and open it in any PDF reader.
- **Folder input → one `.zip`.** Download it, extract it, and open the PDFs inside. The folder layout matches what you put in.

Because the output is always a single file, there is no guesswork about which artifact to grab from a completed run.

## 🧪 Examples

### Nested lists

Markdown lists with multiple levels convert into properly indented PDF lists. Deeply nested outlines, checklists, and multi-level bullet structures stay readable in the final document instead of collapsing into a flat block of text.

### Images and captions

Images referenced in your Markdown are placed into the PDF with their captions. This is useful for documentation pages that combine screenshots with explanatory text, such as step-by-step guides and product walkthroughs.

### Screenshots and section headings

Long documents with many section headings keep their structure. Headings, subheadings, and screenshot blocks are laid out in reading order, so the PDF looks like the document you wrote rather than a raw dump of text.

### Single file conversion

Point the action at `guide.md`. Collect `guide.pdf`. Send it to a colleague or attach it to a ticket.

### Folder conversion

Point the action at a `docs` folder containing `intro.md`, `setup.md`, and `reference/api.md`. Collect one `.zip`. Extract it and you will find `intro.pdf`, `setup.pdf`, and `reference/api.pdf` in the same folder arrangement.

## ✅ Rules to Remember

- Linux x86_64 runners only — use `runs-on: ubuntu-latest`.
- Self-hosted runners must provide Bash, GNU coreutils/findutils, and `zip` on `PATH`.
- Public open source repositories only. Private repositories are rejected by the visibility check.
- Nothing is downloaded at runtime. The converter ships with the repository.
- One input, one output file. Always.

## 🛠️ Troubleshooting

**The run stops immediately with a visibility message.** The converter checks repository visibility through the GitHub API and refuses to run on non-public repositories. Confirm the repository is public before starting the workflow.

**The run fails on a self-hosted machine.** Confirm that Bash, GNU coreutils/findutils, and `zip` are all available on `PATH`. Missing `zip` is a common cause of failure when building the folder archive.

**The run fails on a non-Linux runner.** This action is built for Linux x86_64 runners only. Use `runs-on: ubuntu-latest`.

**I expected several files but got one.** That is correct behavior. File input returns one PDF; folder input returns one ZIP containing all the PDFs.

**My folder had only one Markdown file and I still got a ZIP.** This is intentional. Folder input always produces a ZIP so the output type stays predictable.

**A Markdown file in my folder was skipped.** The action looks for `.md` files recursively. Check the file extension and confirm the file sits inside the folder you pointed at.

## 📚 About the Converter

The conversion engine is iText, and the converter is a script committed directly to this repository. That means every run uses the same known version — no surprise updates, no network fetches in the middle of a job, and no dependency on an external download server being available.

If you need to audit what runs, open `bin/itext-markdown2pdf` in the repository. The licensing terms are in the `LICENSE` file at the repository root.

Keywords: markdown to pdf, github action, itext, pdf converter, markdown, pdf generation, ci cd, automation, documentation, ubuntu runner