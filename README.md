# **Klok Caption Tagger v1 ⏰**

**A powerful, browser-based tool for creating and managing training datasets for AI image generation, such as making LoRAs for the Z-Image model, Stable Diffusion, Flux, Illustrious, and more!**

[![Join Discord](https://img.shields.io/badge/Discord-Join%20Umi%20AI-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/9K7j7DTfG2)

### [**Umi AI Comfy Wildcards**](https://github.com/Tinuva88/Comfy-UmiAI/tree/main/wildcards)

Klok Caption Tagger (KCT) streamlines the tedious process of preparing images for training. It offers a suite of client-side tools including AI-powered auto-tagging, auto-captioning, and recursive folder management. It runs entirely in your browser, keeping your data private and secure.

<img width="1515" height="748" alt="image" src="https://github.com/user-attachments/assets/b8a60572-5891-492a-8c27-774c65bafea7" />

<img width="901" height="735" alt="image" src="https://github.com/user-attachments/assets/92491a5c-e6a7-4953-b927-e93dd98f73ac" />

<img width="1025" height="840" alt="image" src="https://github.com/user-attachments/assets/91f50e68-730d-4812-8d47-53ee1a46aeb2" />

## **Key Features**

*   **Recursive Folder Support**: Load a root folder and KCT will load all images within it, maintaining the subfolder structure.
*   **Multi-Model AI Support**: Connect to the best LLMs available.
    *   **Google Gemini**: Free tier available (Gemini 2.0 Flash, etc.).
    *   **OpenAI**: Support for GPT-4o and variants (Requires paid API key).
    *   **Anthropic**: Support for Claude 3.5 Sonnet/Haiku (Requires paid API key).
*   **Smart Auto-Captioning & Tagging**:
    *   **Batch Control**: Choose to **Ignore** existing text, **Append** to the end, or **Overwrite** completely.
    *   **Retry Logic**: KCT automatically retries failed API requests (up to 3 times) with a cooldown to handle rate limits gracefully.
    *   **Prompt Presets**: Save your favorite system prompts (e.g., "Danbooru Style", "Natural Language") and switch between them instantly.
*   **Flexible Exports**:
    *   **Save to Zip**: Download the whole dataset structure as a compressed file.
    *   **Save to Folder**: Export text files directly back to your local folder, preserving the directory layout and existing filenames.
*   **Global Trigger Word**: Easily set a trigger word that is automatically enforced as the first element of every caption.
*   **Data Persistence**: The tool remembers your API keys, model choices, and presets between sessions.
*   **Tag Management**: 
    *   **Tag Viewer**: Analyze tag frequency across your dataset.
    *   **Tag Mode vs Caption Mode**: Switch the UI to optimize for comma-separated tags or block text captions.

## **Changes from TagPilot [(Original tool by vavo)](https://github.com/vavo/TagPilot "TagPilot HTML code by vavo on Github")**

*   **No Image Renaming**: KCT respects your existing filenames. When exporting, it keeps the original names and directory structure.
*   **Cropping Removed**: The cropping tool has been deprecated to focus on captioning speed and accuracy. (May be re-added via user request).
*   **Direct File System Access**: Now supports writing directly to disk (Chrome/Edge/Brave only).

## **Setup & Installation**

Since KCT is a client-side application, there is no Python backend or Node.js server required.

1.  **Clone or Download the Repository**
    ```bash
    git clone https://github.com/Klokinator/KlokCaptionTagger.git
    ```
2.  **Run the Application**
    Simply double-click `KlokCaptionTagger.html` to open it in your web browser.

## **Usage Workflow**

1.  **Load Data**: 
    *   **Choose Folder**: Select a folder to recursively load images and existing `.txt` files.
    *   **Upload Zip**: Upload a generic dataset zip.
2.  **Configure Models**: 
    *   Click **"Model Settings"**.
    *   Select your provider (Gemini, OpenAI, or Anthropic).
    *   Enter your API Key.
    *   Select the specific model ID you wish to use from the table.
3.  **Tagging/Captioning**:
    *   Click **"Tag All"** or **"Caption All"**.
    *   Select a **Preset** or write a custom System Prompt.
    *   Set your **Limits** (Max tags or Max words).
    *   Choose a mode (Ignore/Append/Overwrite) and start.
4.  **Review**:
    *   Use the **Tag Viewer** to clean up unwanted tags globally.
    *   Click on individual text boxes to perform manual edits.
5.  **Export**:
    *   **Save to Folder**: Updates the `.txt` files in your actual directory (requires permission).
    *   **Save to Zip**: Downloads a standalone package.

## **Technology Stack**

*   **HTML5 / JavaScript (ES6+)**: Core logic.
*   **Tailwind CSS**: UI styling (loaded via CDN).
*   **JSZip**: Client-side archiving.
*   **File System Access API**: For direct folder reading/writing.
*   **LocalStorage**: For saving user preferences.

---

Klok Caption Tagger is based on the excellent [TagPilot HTML code by vavo on Github](https://github.com/vavo/TagPilot "TagPilot HTML code by vavo on Github")! His version has Cropping and mine does not (yet?) so check his program out too!

### [**Umi AI Comfy Wildcards**](https://github.com/Tinuva88/Comfy-UmiAI/tree/main/wildcards)

[![Join Discord](https://img.shields.io/badge/Discord-Join%20Umi%20AI-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/9K7j7DTfG2)
