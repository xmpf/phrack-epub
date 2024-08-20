## Phrack Magazine EPUB

Phrack Issues in EPUB format for e-readers (e.g: Kindle)

Render txt as PDF:

```
google-chrome-stable --incognito --headless --disable-gpu --no-pdf-header-footer --print-to-pdf="$file.pdf" --no-margins "http://www.phrack.org/archives/issues/$ch/$file"
```

Convert PDF to EPUB:

```
find . -iname "*.pdf" -type f | xargs -I% -P4 bash -c "echo -e \"\e[1mConverting file % \e[0m\" ; ebook-convert \"%\" \"${%%.pdf}.epub\" &>/dev/null; rm -f \"%\""
```

