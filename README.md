# Voice Assistant for Files and the Web

## Summary
A voice assistant that understands speech, searches and analyses information on the internet, and saves the results into files (notes, summaries, lists) on request. For example: "Find three recent articles about solar panels, summarize them, and save the summary to solar.md."

## Background
Collecting information from the internet and organizing it takes time. You have to open a browser, read several pages, pick out the main points, and write them down by hand. This is especially inconvenient when your hands are busy or you need to take a quick note. The assistant reduces this process to a single voice command. It can be useful for students, people with visual or motor impairments, and anyone who takes notes often.

## How is it used
1. The user speaks a command into the microphone.
2. The assistant converts the speech to text and works out what to do: search, summarize, or save.
3. The assistant searches the web, reads the pages, and prepares a short summary.
4. Before saving, it reads the result aloud and asks for confirmation.
5. After confirmation, it creates or updates a file in a pre-selected folder.

## Data sources and AI methods
- **Speech recognition (speech-to-text):** ready-made models such as Whisper.
- **Command understanding:** a large language model identifies the user's intent ("search", "save", "read a file").
- **Web search and analysis:** a search API, followed by text extraction from the pages and summarization by a language model.
- **Speech synthesis (text-to-speech):** so the assistant can answer out loud.
- **Data:** no custom training data is needed. The system uses pre-trained models and publicly available web pages.

## Challenges
- **Errors and made-up facts.** The model may summarize a source incorrectly, so the assistant should always include links to its sources.
- **File safety.** The assistant must not delete or overwrite important files. It works only in one chosen folder and asks for confirmation before saving.
- **Privacy.** Voice recordings and queries may contain personal information, so they should be handled carefully and not stored longer than necessary.
- **Recognition quality.** Background noise and strong accents can reduce accuracy.
- **Reliability of sources.** The internet contains a lot of inaccurate information, so the assistant should compare several sources.

## What next
- Add calendar and reminder features.
- Teach the assistant to read and edit existing documents.
- Support multiple languages.
- Remember user preferences (note format, favorite sources).

## Acknowledgments
- Building AI course (Reaktor and the University of Helsinki).
- Open-source speech recognition models and language models.
