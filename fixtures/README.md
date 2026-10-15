# Fixtures for PdfCraft issue reports

Synthetic one-page PDF (`scheda.pdf`, written by LibreOffice, DejaVu Sans TrueType subsets) and the
`pdfcraft-cli run --script` steps (`edits.json`) used in:

- the comment on storytold/pdfcraft#730 (blurry text at 96 dpi): `body_10pt_before_after.png`,
  `regions_before_after_poppler.png`;
- "Edit text: the rewritten paragraph is emitted before the backgrounds drawn between its rows":
  `cmp_edit_A_titolo.png`, `poppler_A_crop.png`;
- "Edit text: one character outside the subset switches the whole line to Helvetica":
  `cmp_edit_C_data.png`, `cmp_edit_D_glifo_mancante.png`.

The text in the PDF is placeholder text; no real document is included.

`scanned_card.pdf` is the same card rendered to a 288 dpi JPEG and wrapped as a one-image page
(a "scan"), used in "Shrunk images without /Interpolate are nearest-sampled: scanned text comes
out ragged": `scanned_card_61dpi_before_after.png`.

`ocr_card.pdf` is `scanned_card.pdf` passed through Tesseract 5 (`tesseract scan.jpg out pdf`): the
same image with an invisible GlyphLessFont text layer, used in "Edit text on an OCR layer: a line
edit shows nothing, a paragraph edit draws boxes": `ocr_edits.json`, `ocr_edit_before_after.png`.
