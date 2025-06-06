# Moodle Quiz XML Parser

Quick tool to parse quiz questions export from moodle in the [Moodle XML format](https://docs.moodle.org/403/en/Moodle_XML_format) and render them to human-readable text files for editing. Inspired by [moodlexml.fly.dev](https://moodlexml.fly.dev/converter/quiz).

## Usage

1. `git clone` the monorepo
2. `cd` into the `parse-moodle-xml` directory
3. Run `npm install`
4. [Export quiz questions](https://nonproliferation-elearning.eu/question/bank/exportquestions/export.php) one unit at a time, ensuring `File Format: Moodle XML` and `Write category to file` are selected and place the files in the `/data` folder.
5. Run `node .` to convert the data to markdown

### Converting to Word Docs

1. Install [Pandoc](https://pandoc.org/index.html) for your platform
2. Run `bash markdownToDoc.bash` to convert the data first to markdown, then to docx.

## Notes

- This produces output similar to Moodle's [Aiken](https://docs.moodle.org/403/en/Aiken_format) format, but that only supports multiple choice questions
- [Moodle2Word](https://docs.moodle.org/403/en/Word_table_format) might be a more feature-complete alternative to this script
