# Ruyi DOCX

`src/docx` is a standalone Python package for deterministic Word document creation and editing. The import package is named `ruyi_docx` so it does not shadow the third-party `python-docx` package named `docx`.

## Capabilities

- Typed document specifications for headings, paragraphs, lists, tables, images, and page breaks.
- A4/landscape page layout, Chinese fonts, heading hierarchy, headers, footers, and page numbers.
- Structured reading and plain-text extraction.
- Cross-run replacement in body text, nested tables, headers, and footers.
- Append, paragraph deletion, and named-style application.
- Optional `docxtpl` template rendering and `docxcompose` merging.
- LibreOffice headless PDF rendering with explicit failure reporting.
- ZIP integrity, required OOXML parts, and readability validation.
- Path-restricted MCP adapter and an AI Skill operating guide.

## Development

From this directory, with the package dependencies available:

```powershell
python -m pytest
```

Install optional capabilities only when needed:

```powershell
pip install -e ".[templates,mcp,test]"
```

The core package does not require LibreOffice. PDF rendering reports a `RenderError` when no renderer is available.

