<a target="_blank" href="https://colab.research.google.com/github/DoIT-Artifical-Intelligence/colab-ytt-to-docs/blob/main/Colab_YouTube_Transcription_Extractor.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

# Colab YouTube Transcription Extractor and Summarizer

Extract YouTube video transcripts and save them directly to Google Docs using Google Colab. Optionally, uses AI to summarize the transcript.

## Features
- Fetches YouTube video transcripts using the [youtube-transcript-api](https://github.com/jdepoix/youtube-transcript-api)
- Saves the transcript to a new Google Doc in your Google Drive
- Saves an AI summary to a new Google Doc in your Google Drive

## How to Use in Google Colab

1. **Open Google Colab**
	- Go to [Google Colab](https://colab.research.google.com/).
2. **Upload the Notebook**
	- Download `Colab_YouTube_Transcription_Extractor.ipynb` from this repository.
	- In Colab, click `File > Upload notebook` and select the file.
3. **Set the YouTube URL and API Key**
	 - In the first cell, replace the sample URL and title fallback with details for your target YouTube video link:
		 ```python
		 YOUTUBE_URL = "https://www.youtube.com/watch?v=XXXXXXXXXXX"
         VIDEO_TITLE_FALLBACK = "INSERT VIDEO NAME"
		 ```
	 - Add your YouTube Data API key to Colab secrets:
		 - In Colab, go to `Runtime > Manage secrets` and add a new secret named `YOUTUBE_DATA_API_KEY` with your API key value.
         - Check the "Notebook access" toggle.
	     - To register for a YouTube Data API key:
		     1. Go to the [Google Cloud Console](https://console.cloud.google.com/).
		     2. Create a new project (or select an existing one).
		     3. Enable the YouTube Data API v3 for your project.
		     4. Go to `APIs & Services > Credentials` and create an API key.
		     5. Copy the API key and add it to Colab secrets as described above.
4. **Set the Gemini API Key**
    - Add your Gemini API key to Colab secrets:
        - In Colab, go to `Runtime > Manage secrets` and add a new secret named `GEMINI_API_KEY` with your API key value.
        - To register for a Gemini API key:
            1. Go to the [Google Cloud Console](https://console.cloud.google.com/).
            2. Create a new project (or select an existing one).
            3. Go to [Credentials](https://console.cloud.google.com/apis/credentials).
            4. Create key which has restrictions to Generative Language API
            5. Copy the API key and add it to Colab secrets as described above.
5. **Run All Cells**
	- Click `Runtime > Run all` to execute the notebook.
	- Authenticate with your Google account when prompted.
	- Provide your YouTube Data API key if required.
	- **Note:** The notebook will ask for access to your Google Drive in order to create the transcript file. You must grant access to proceed.
6. **Get the Transcript**
	- The notebook will fetch the transcript and create a new Google Doc in your Drive.
	- A shareable link to the document will be printed at the end.
7. **Get the AI Summary** (optional)
    - The notebook will create a new Google Doc in your Drive.
    - A shareable link to the document will be printed at the end.

## Requirements
- Google Colab
- YouTube Data API key (for fetching video title)
- Gemini API key (for AI summary)
- Access to Google Drive

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
