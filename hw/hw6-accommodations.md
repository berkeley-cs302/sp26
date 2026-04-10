---
lang: en
title: Accommodations Policies & Document Remediation
number: 6
permalink: /sp25/hw/hw6/
layout: hw
due_date: Wednesday, April 15, 2026
peer_review_date: Friday, April 17, 2026
responses_doc: https://docs.google.com/document/d/1nUg_PiFqOcRB6qL8GDUc0HfSovTZAoEz5Esu1thlOwc/edit?usp=sharing
---

[accommodations_wrong]: https://drive.google.com/file/d/1LtQxWKej-XsDKIIyk35fONZXsT1juEpz/view?usp=share_link
[shutting_out]: https://drive.google.com/file/d/10-rXEcdijXgVyxSvelvZRGPUX7A63Bul/view?usp=share_link
[stanford_disabled]: https://drive.google.com/file/d/1ZB6ukQ8D-Nog4cKA_jTfmwiBIbdp1N4T/view?usp=share_link
[dsp_home]: https://dsp.berkeley.edu/home
[dsp_instructor_guide]: https://teaching.berkeley.edu/resources/instructor-guide-dsp-accommodations
[dap_pdfs]: https://dap.berkeley.edu/documents-forms/pdfs
[ally_bcourses]: https://rtl.berkeley.edu/services-programs/ally-bcourses
[ally_instructor_report]: https://rtl.berkeley.edu/services-programs/course-design-tools/quality-assurance-qa/check-accessibility-ally-instructor
[rtl_accessibility]: https://rtl.berkeley.edu/resources/accessibility-teaching-learning
[ada_title_ii]: https://ue.berkeley.edu/news/ada-title-ii-update-new-requirements-digital-course-content-accessibility
[rtl_accessible_pdfs]: https://rtl.berkeley.edu/accessible-pdf-files
[overleaf_accessible_pdfs]: https://docs.overleaf.com/writing-and-editing/creating-accessible-pdfs
[accessible_latex_repo]: https://github.com/rhstanton/accessible_LaTeX?tab=readme-ov-file

Your course materials need to be accessible to all students. In this assignment, you will learn about disability accommodation policies, audit PDF files used in your course, and practice document remediation. You will also reflect on how UC Berkeley's [Disabled Students' Program (DSP)][dsp_home] serves students with disabilities.

**Context:** As of April 24, 2026, all digital course materials at UC Berkeley — including content inside bCourses — must meet [WCAG 2.1 Level AA][ada_title_ii] standards under the updated ADA Title II requirements.

## Required Reading

Read these three articles and leave at least 1 comment on each in the shared document:

- [<u>Are Colleges Getting Disability Accommodations All Wrong?</u>][accommodations_wrong]
- [<u>How Universities Are Shutting Out Disabled Students and Staff (The Walrus)</u>][shutting_out]
- [<u>Nearly 40% of Stanford undergraduates claim they're disabled. I'm one of them.</u>][stanford_disabled]

## Part 1: PDF Document Remediation

### 1a. Select Two PDF Files

Pick **2 PDF files** currently used in your course (e.g., homework, lab, lecture slides, exam, syllabus). These should be files that students are expected to read or interact with.

### 1b. Audit Your PDFs

Run each PDF through **at least two** of the following checkers:

1. **[pdf4wcag.com](https://pdf4wcag.com)** — Select the **WCAG 2.2** profile. Also try the **WCAG 2.2 Human and Machine** test, which uses an experimental AI model to evaluate semantic tag usage.
2. **[veraPDF](https://verapdf.org/)** — The open-source industry-standard validator. You can use the [web demonstrator](https://demo.verapdf.org/) or install locally (requires Java). Select the **PDF/UA-1** validation profile.
3. **Adobe Acrobat Pro** — Use the built-in Accessibility Check (Full Check) under Tools → Accessibility. Available via [UC Berkeley software](https://software.berkeley.edu/adobe). See [Checking PDFs in Acrobat](#checking-pdfs-in-acrobat) below.

**Optional:** If you are a TA or instructor of record in a bCourses site, you can also use the **[Ally accessibility checker][ally_bcourses]** built into bCourses. Ally provides per-file accessibility scores and remediation suggestions. You can generate an [Ally Instructor Report][ally_instructor_report] to see all issues across your course site. *(Note: Ally is only available if you have an instructor or TA role in the course.)*

### 1c. Attempt Remediation

Based on the audit results, try to fix some of the issues you found. You don't need to spend too much time getting things perfect — the goal is to understand the process and the challenges involved.

Some approaches to try:

- If the source file is available (e.g., Word, Google Docs, LaTeX, Typst), fix issues at the source and re-export.
- If only the PDF is available, try using Adobe Acrobat Pro's accessibility tools to add tags, alt text, or fix reading order.
- For scanned / image-only PDFs, run OCR first (Acrobat Pro or [SensusAccess via bCourses](https://accesscontent.berkeley.edu/)).

See [Guidelines and Testing of PDF Files](#guidelines-and-testing-of-pdf-files) below for more detail.

## Part 2: Written Responses

Answer the following on the responses document:

### 2a. Reflections on DSP and Accommodations

Based on the readings and your own experiences at Berkeley, do you think the [DSP program][dsp_home] is serving students well? What changes, if any, would you like to see? You may also want to review the [Instructor Guide to DSP Accommodations][dsp_instructor_guide].

### 2b. Draft Extension & Accommodation Policies

Draft some sample policies for assignment extensions and accommodations (labs, homework, projects). What kinds of late policies would you choose? Write a few sentences explaining why you think these are good. Consider:

- How many late days or slip days will you offer?
- Will you use a tool like [Flextensions](https://github.com/cs169/flextensions)?
- How will you handle DSP accommodations for deadlines?
- How will you communicate these policies to students?

### 2c. PDF Remediation Report

For each of the two PDFs you tested:

1. Link to the file (or describe it if not publicly available).
2. What was the source format? (Word, LaTeX, Typst, Google Docs, HTML, scanned, unknown, etc.)
3. What were the results of the accessibility audit? Summarize the top issues found.
4. What remediation steps did you attempt, and what was the result?

### 2d. Process Reflection

After auditing your course website (HW5) and now auditing and remediating PDF files, share your experiences about the process. What was harder than expected? What tools were most or least helpful? What would you change about how your course produces documents?

---

## Guidelines and Testing of PDF Files

### Why PDFs Are Hard for Accessibility

PDFs were designed as a fixed-layout print format — they describe *where* content appears on a page, not *what* it means. Without explicit structure tags, a PDF is essentially a collection of positioned glyphs and images. Screen readers cannot determine reading order, distinguish headings from body text, or interpret tables without this semantic layer. This is why the [UC Berkeley Digital Accessibility Program recommends][dap_pdfs] using HTML, Google Docs, or other editable formats when possible, and treating PDF as a last resort.

That said, PDFs are often necessary for exams, formal handouts, and archival documents. When you must use PDF, the goal is to produce a **tagged PDF** that conforms to [PDF/UA (ISO 14289)](https://pdfa.org/resource/pdf-ua-iso-14289/) and WCAG 2.1 Level AA.

### Checking PDFs in Acrobat

If you have access to Adobe Acrobat Pro (available via [software.berkeley.edu](https://software.berkeley.edu/adobe)):

1. Open the PDF and go to **Tools → Accessibility**.
2. Run **Full Check** (Accessibility Check). Select WCAG 2.1 AA as the standard.
3. Review the results panel — issues are categorized (document, page content, forms, tables, etc.).
4. Use the **Reading Order** tool to inspect and fix the tag structure.
5. Use the **Set Alternate Text** tool for images.
6. Check the **Tags** panel to verify the document's logical structure tree.

**Important:** Acrobat's checker does not catch all issues. A passing result in Acrobat does not guarantee full accessibility — always also test with a screen reader and/or an external validator like veraPDF.

### Testing with Screen Readers

Testing with an actual screen reader is the most reliable way to verify accessibility. Try navigating your PDF without looking at the screen.

**macOS — VoiceOver:**

1. Open the PDF in Preview or Adobe Acrobat Reader.
2. Press **⌘ + F5** to enable VoiceOver.
3. Use **VO + →** (Control + Option + Right Arrow) to navigate through elements.
4. Listen for: correct reading order, headings announced as headings, alt text read for images, table headers announced.
5. Press **⌘ + F5** again to disable VoiceOver.

**Windows — Narrator or NVDA:**

1. Open the PDF in Adobe Acrobat Reader.
2. **Narrator:** Press **Win + Ctrl + Enter** to toggle Narrator.
3. **NVDA** (free, recommended): Download from [nvaccess.org](https://www.nvaccess.org/download/). Press **Insert + ↓** to start reading.
4. Navigate by headings (**H** key), tables (**T** key), and links (**K** key).

### Typst Accessibility

[Typst](https://typst.app/) (v0.14+) produces **tagged PDFs by default**, making it one of the easiest paths to accessible PDF output from a markup language. Key features:

- Tags are generated automatically from semantic elements (headings, lists, figures, etc.) — no extra packages needed.
- Opt-in support for **PDF/UA-1** conformance with stricter validation.
- Use the `alt` parameter on `figure` to provide alt text for diagrams and images.
- Built-in validation will **fail the compile** if PDF/UA-1 conformance is requested and requirements aren't met (e.g., missing alt text, missing document title).

```typst
// Enable PDF/UA-1 conformance
#set document(title: "My Accessible Exam", date: auto)
// pdf-standard: "ua-1" can be set via CLI or export settings

#figure(
  image("diagram.png"),
  alt: "Flowchart showing three stages of compilation: parse, type-check, emit.",
  caption: [The compilation pipeline.],
)
```

Resources:
- [Typst Accessibility Guide](https://typst.app/docs/guides/accessibility/)
- [Blog: How to create accessible PDFs from the start](https://typst.app/blog/2025/accessible-pdf/)
- [Typst PDF export documentation](https://typst.app/docs/reference/pdf/)
- [Quarto PDF Accessibility with Typst and LaTeX](https://quarto.org/docs/blog/posts/2026-03-05-pdf-accessibility-and-standards/index.html)

### LaTeX Accessibility

LaTeX has historically produced **untagged, inaccessible PDFs**. The [LaTeX Tagged PDF Project](https://github.com/latex3/tagging-project) has made significant progress, but support is still evolving. As of TeX Live 2025 with LuaLaTeX:

- Basic document structure tagging (headings, paragraphs) works with `\DocumentMetadata`.
- PDF/UA-2 conformance is possible for straightforward documents.
- MathML embedding for accessible math is supported but viewer support is inconsistent (best with Adobe Reader 2025 + NVDA on Windows).
- Many common packages (e.g., `beamer`) are **not yet compatible** with tagging. Check the [LaTeX Tagging Project package status list](https://github.com/latex3/tagging-project/blob/main/documentation/supported-packages.md).

```latex
% Minimal tagged PDF setup (requires LuaLaTeX + TeX Live 2025)
\DocumentMetadata{
  lang = en,
  pdfstandard = ua-2,
  pdfstandard = a-4,
  testphase = phase-III
}
\documentclass{article}
\usepackage{unicode-math}
\begin{document}
\section{Accessible Section}
The quadratic formula: \( x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a} \)
\end{document}
```

**Be aware:** The LaTeX tagging infrastructure is under active development. Package compatibility issues are common, and not all document types can produce fully accessible output yet. Always validate with veraPDF after compilation.

Resources:
- [Overleaf: Creating accessible PDFs in LaTeX][overleaf_accessible_pdfs]
- [accessible_LaTeX — Example templates and guide][accessible_latex_repo]
- [eSAIL: Creating Accessible LaTeX PDFs (PDF/UA-2 in Overleaf)](https://esail.tamu.edu/faculty-tutorials/accessible-latex-pdf-ua-2-overleaf-2025/)
- [TUG: Accessibility and PDF Standards](https://www.tug.org/twg/accessibility/)
- [tagpdf package on CTAN](https://ctan.org/pkg/tagpdf)

### Alternative: Export to HTML

Given the difficulty of making PDFs fully accessible, consider **also providing an HTML version** of your documents. HTML is natively accessible when authored with semantic markup and is far easier to make WCAG-compliant than PDF.

**Pandoc** can convert from LaTeX, Typst, Markdown, and many other formats to HTML with MathJax for math rendering:

```bash
# LaTeX to HTML with MathJax
pandoc input.tex -o output.html --mathjax --standalone

# Markdown to HTML
pandoc input.md -o output.html --mathjax --standalone
```

- [Pandoc documentation](https://pandoc.org/MANUAL.html)

**Typst** can export directly to HTML (experimental as of v0.14):

```bash
typst compile input.typ output.html
```

- [Typst HTML export documentation](https://typst.app/docs/reference/html/)

Providing both a PDF and an HTML version of key course documents is a practical way to meet accessibility requirements while preserving the layout you need for exams and printed materials.

### AI-Assisted PDF Remediation Tools

Several AI-powered tools can help with large-scale or complex PDF remediation. These are **not required** for this assignment, but are worth knowing about:

- **[PDFix](https://pdfix.net/)** — Free desktop app (PDFix Desktop Lite) with veraPDF validation built in. Pro version has AI auto-tagging. Cross-platform.
- **[PREP (Continual Engine)](https://www.continualengine.com/prep/)** — AI-powered remediation platform. Used by Stanford. Auto-tags ~90% of content. [TODO: Check if UC Berkeley has a license]
- **[pdf4wcag.com](https://pdf4wcag.com)** — Free web-based checker using veraPDF with experimental AI-based "Human and Machine" WCAG checks.
- **[PAC 2026 (beta)](https://pdfa.org/pdf-accessibility-checker-pac-now-with-ai/)** — Free PDF Accessibility Checker with new AI tab for evaluating semantic structure (Windows only).
- **[OpenDataLoader](https://github.com/opendataloader-project/opendataloader-pdf)** — Open-source audit→auto-tag→PDF/UA pipeline (auto-tagging coming Q2 2026).

[TODO: Add any Berkeley-specific tools or licenses here]

---

## UC Berkeley Resources

- [Digital Accessibility Program (DAP)](https://dap.berkeley.edu/) — Campus hub for digital accessibility guidance
- [DAP: PDFs][dap_pdfs] — Specific guidance on PDF accessibility at Berkeley
- [RTL: Accessible PDF Files][rtl_accessible_pdfs] — Step-by-step guide for making PDFs accessible
- [Accessibility in Teaching & Learning (RTL)][rtl_accessibility] — Resource hub for instructors
- [Ally in bCourses][ally_bcourses] — Built-in accessibility checker for course content
- [Accessible bCourses Sites](https://rtl.berkeley.edu/accessible-bcourses-sites) — Guide to building accessible Canvas sites
- [Disabled Students' Program][dsp_home] — Accommodation services for students
- [Instructor Guide to DSP Accommodations][dsp_instructor_guide] — CTL guide for faculty
- [ADA Title II Update for Berkeley][ada_title_ii] — Overview of the April 2026 deadline
- [Disability Access & Compliance (DAC)](https://dac.berkeley.edu/) — Campus compliance office
- [Report a Web Accessibility Issue](https://dap.berkeley.edu/report-web-accessibility-issue)

## Rubric (Do this for full credit)

- (Individual) Left 1 or more comments on [<u>Are Colleges Getting Disability Accommodations All Wrong?</u>][accommodations_wrong]
- (Individual) Left 1 or more comments on [<u>How Universities Are Shutting Out Disabled Students and Staff</u>][shutting_out]
- (Individual) Left 1 or more comments on [<u>Nearly 40% of Stanford undergraduates claim they're disabled.</u>][stanford_disabled]
- (Individual) Part 1: PDF audit results for 2 files using at least 2 tools, with attempted remediation
- (Individual) Part 2a: Reflection on DSP and accommodations
- (Individual) Part 2b: Draft extension/accommodation policies with explanation
- (Individual) Part 2c: PDF remediation report (links, source format, audit results)
- (Individual) Part 2d: Process reflection on website + PDF auditing experience
- (Due 2:00 PM Thursday) (Individual) Left 1 or more comments on 2 other courses' responses
