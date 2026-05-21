Of course. Here is the complete English translation of the README.md file. I've added a note at the top as you requested and ensured the technical instructions remain accurate.

***

> **Note**
>
> This document has been translated from the original Chinese README. Some functionality within the program has also been partially translated into English.

> **Note**
>
> The new pip packages for the Gradio component that this project depends on (Gradio 3.26~3.27) have serious bugs. Therefore, please strictly select the **specified versions** in `requirements.txt` during installation.
>
> `pip install -r requirements.txt -i https://mirrors.aliyun.com/pypi/simple/`

# <img src="docs/logo.png" width="40" > ChatGPT Academic Optimization

**If you like this project, please give it a Star; if you have developed more useful shortcuts or function plugins, feel free to open an issue or pull request.**

We also have a README in [English|](docs/README_EN.md)[日本語|](docs/README_JP.md)[Русский|](docs/README_RS.md)[Français](docs/README_FR.md) translated by this project itself.

> **Note**
>
> 1. Please note that only function plugins (buttons) marked in **red** support reading files. Some plugins are located in the **dropdown menu** in the plugin area. We welcome and prioritize PRs for any new plugins!
>
> 2. The function of each file in this project is explained in detail in the self-analysis report [`self_analysis.md`](https://github.com/binary-husky/chatgpt_academic/wiki/chatgpt-academic%E9%A1%B9%E7%9B%AE%E8%87%AA%E8%AF%91%E8%A7%A3%E6%8A%A5%E5%91%8A). As the version iterates, you can also click the relevant function plugins at any time to have GPT regenerate the project's self-analysis report. A summary of frequently asked questions can be found in the [`wiki`](https://github.com/binary-husky/chatgpt_academic/wiki/%E5%B8%B8%E8%A7%81%E9%97%AE%E9%A2%98).
>
> 3. Co-existence of OpenAI and API2D API keys is now supported. You can fill them in the configuration file like `API_KEY="openai-key1,openai-key2,api2d-key3"`. To temporarily change the `API_KEY`, simply type the temporary `API_KEY` in the input box and press Enter to apply it.

<div align="center">

Function | Description
--- | ---
One-Click Polish | Supports one-click polishing and finding grammatical errors in papers.
One-Click Chinese-English Translation | One-click mutual translation between Chinese and English.
One-Click Code Explanation | Correctly displays and explains code.
[Custom Shortcuts](https://www.bilibili.com/video/BV14s4y1E7jN) | Supports custom shortcuts.
[Configure Proxy Server](https://www.bilibili.com/video/BV1rc411W7Dr) | Supports proxy connections to OpenAI/Google, etc., instantly unlocking ChatGPT's [real-time information aggregation](https://www.bilibili.com/video/BV1om4y127ck/) capability on the internet.
Modular Design | Supports powerful custom [function plugins](https://github.com/binary-husky/chatgpt_academic/tree/master/crazy_functions), with plugin [hot-reloading](https://github.com/binary-husky/chatgpt_academic/wiki/%E5%87%BD%E6%95%B0%E6%8F%92%E4%BB%B6%E6%8C%87%E5%8D%97) support.
[Self-Program Analysis](https://www.bilibili.com/video/BV1cj411A7VW) | [Function Plugin] [One-click to understand](https://github.com/binary-husky/chatgpt_academic/wiki/chatgpt-academic%E9%A1%B9%E7%9B%AE%E8%87%AA%E8%AF%91%E8%A7%A3%E6%8A%A5%E5%91%8A) the source code of this project.
[Program Analysis](https://www.bilibili.com/video/BV1cj411A7VW) | [Function Plugin] One-click analysis of other Python/C/C++/Java/Lua/... project trees.
Read Papers | [Function Plugin] One-click to read the full text of a LaTeX paper and generate a summary.
LaTeX Full-Text [Translation](https://www.bilibili.com/video/BV1nk4y1Y7Js/)/[Polishing](https://www.bilibili.com/video/BV1FT411H7c5/) | [Function Plugin] One-click translation or polishing of LaTeX papers.
Batch Comment Generation | [Function Plugin] One-click batch generation of function comments.
Chat Analysis Report Generation | [Function Plugin] Automatically generates a summary report after running.
Markdown [Chinese-English Translation](https://www.bilibili.com/video/BV1yo4y157jV/) | [Function Plugin] See the [README](https://github.com/binary-husky/chatgpt_academic/blob/master/docs/README_EN.md) in 5 languages above? It was done with this.
[Arxiv Assistant](https://www.bilibili.com/video/BV1LM4y1279X) | [Function Plugin] Input an Arxiv article URL to translate the abstract and download the PDF in one click.
[PDF Paper Full-Text Translation](https://www.bilibili.com/video/BV1KT411x7Wn) | [Function Plugin] Extracts title & abstract from PDF papers + translates the full text (multi-threaded).
[Google Scholar Integration Assistant](https://www.bilibili.com/video/BV19L411U7ia) | [Function Plugin] Given any Google Scholar search page URL, let GPT help you [write related works](https://www.bilibili.com/video/BV1GP411U7Az/).
Formula/Image/Table Display | Can display formulas in both [TeX and rendered forms](https://user-images.githubusercontent.com/96192199/230598842-1d7fcddd-815d-40ee-af60-baf488a199df.png), supports formula and code highlighting.
Multi-threaded Function Plugin Support | Supports multi-threaded calls to ChatGPT to process [massive amounts of text](https://www.bilibili.com/video/BV1FT411H7c5/) or programs with one click.
Launch with Dark Gradio [Theme](https://github.com/binary-husky/chatgpt_academic/issues/173) | Add `/?__dark-theme=true` to the browser URL to switch to the dark theme.
[Multi-LLM Model](https://www.bilibili.com/video/BV1wT411p7yf) Support, [API2D](https://api2d.com/) Interface Support | Being served by GPT-3.5, GPT-4, and [Tsinghua's ChatGLM](https://github.com/THUDM/ChatGLM-6B) at the same time must feel great, right?
Hugging Face [Online Demo](https://huggingface.co/spaces/qingxu98/gpt-academic) without VPN | After logging into Hugging Face, duplicate [this space](https://huggingface.co/spaces/qingxu98/gpt-academic).
... | ...

</div>

- New Interface (Switch between "Side-by-Side" and "Top-and-Bottom" layouts by modifying the LAYOUT option in `config.py`)
<div align="center">
<img src="https://user-images.githubusercontent.com/96192199/230361456-61078362-a966-4eb5-b49e-3c62ef18b860.gif" width="700" >
</div>

- All buttons are dynamically generated by reading `functional.py`. You can freely add custom functions, liberating your clipboard.
<div align="center">
<img src="https://user-images.githubusercontent.com/96192199/231975334-b4788e91-4887-412f-8b43-2b9c5f41d248.gif" width="700" >
</div>

- Polish / Proofread
<div align="center">
<img src="https://user-images.githubusercontent.com/96192199/231980294-f374bdcb-3309-4560-b424-38ef39f04ebd.gif" width="700" >
</div>

- If the output contains formulas, they will be displayed in both TeX and rendered formats for easy copying and reading.
<div align="center">
<img src="https://user-images.githubusercontent.com/96192199/230598842-1d7fcddd-815d-40ee-af60-baf488a199df.png" width="700" >
</div>

- Too lazy to read the project code? Feed the entire project directly to ChatGPT.
<div align="center">
<img src="https://user-images.githubusercontent.com/96192199/226935232-6b6a73ce-8900-4aee-93f9-733c7e6fef53.png" width="700" >
</div>

- Mixed calls to multiple large language models (ChatGLM + OpenAI-GPT3.5 + [API2D](https://api2d.com/)-GPT4)
<div align="center">
<img src="https://user-images.githubusercontent.com/96192199/232537274-deca0563-7aa6-4b5d-94a2-b7c453c47794.png" width="700" >
</div>

Mixed calls to multiple large language models [Hugging Face Beta Version](https://huggingface.co/spaces/qingxu98/academic-chatgpt-beta) (Hugging Face version does not support ChatGLM).

---

## Installation - Method 1: Direct Run (Windows, Linux or MacOS)

1.  Download the project
    ```sh
    git clone https://github.com/binary-husky/chatgpt_academic.git
    cd chatgpt_academic
    ```

2.  Configure API_KEY and Proxy Settings

    In `config.py`, configure your overseas Proxy and OpenAI API KEY. Instructions are as follows:
    ```
    1. If you are in a region with restricted access, you need to set up an overseas proxy to use the OpenAI API. Please read config.py carefully for setup instructions (1. Change USE_PROXY to True; 2. Modify the proxies according to the instructions).
    2. Configure your OpenAI API KEY. Any number of OpenAI keys and API2D keys can coexist for load balancing. Separate multiple keys with a comma, e.g., API_KEY="OpenAI-key1,API2D-key2,OpenAI-key3,OpenAI-key4"
    3. Issues related to proxy networks (network timeouts, proxy not working) are summarized at https://github.com/binary-husky/chatgpt_academic/issues/1
    ```
    (P.S. The program will first check for a private configuration file named `config_private.py` and use its settings to override the same settings in `config.py`. Therefore, if you understand our configuration logic, we strongly recommend creating a new file named `config_private.py` next to `config.py` and transferring (copying) your configurations there. `config_private.py` is ignored by git, which keeps your private information more secure.)

3.  Install dependencies
    ```sh
    # (Option I: If you are familiar with Python) Recommended
    python -m pip install -r requirements.txt
    # Note: Use the official pip source or an Alibaba mirror. Other pip sources (like some university mirrors) might cause issues. To temporarily change the source: python -m pip install -r requirements.txt -i https://mirrors.aliyun.com/pypi/simple/

    # (Option II: If you are not familiar with Python) Use Anaconda, the steps are similar:
    # (II-1) conda create -n gptac_venv python=3.11
    # (II-2) conda activate gptac_venv
    # (II-3) python -m pip install -r requirements.txt
    ```

    If you need to support the Tsinghua ChatGLM backend, you'll need to install additional dependencies (Prerequisites: familiar with Python + powerful enough computer):
    ```sh
    python -m pip install -r request_llm/requirements_chatglm.txt
    ```

4.  Run
    ```sh
    python main.py
    ```

5.  Test Function Plugins
    ```
    - Test Python project analysis
        (Option 1) In the input area, type `./crazy_functions/test_project/python/dqn`, then click "Analyze Entire Python Project".
        (Option 2) Expand the file upload area, drag and drop a Python file or a zip file containing Python files. After the feedback appears, click "Analyze Entire Python Project".
    - Test self-code analysis (this project analyzing itself)
        Click "[Multi-threaded Demo] Analyze this project itself (source code self-analysis)".
    - Test the function plugin template (asks GPT what happened on this day in history). You can use this as a template to create more complex functions.
        Click "[Function Plugin Template Demo] On This Day in History".
    - The dropdown menu in the function plugin area has more features to choose from.
    ```

## Installation - Method 2: Using Docker

1.  ChatGPT Only (Recommended for most users)
    ```sh
    # Download the project
    git clone https://github.com/binary-husky/chatgpt_academic.git
    cd chatgpt_academic
    # Configure "Overseas Proxy", "API_KEY", and "WEB_PORT" (e.g., 50923), etc.
    Edit config.py with any text editor
    # Build
    docker build -t gpt-academic .
    # (Last step - Option 1) On Linux, using `--net=host` is more convenient
    docker run --rm -it --net=host gpt-academic
    # (Last step - Option 2) On macOS/Windows, you must use the -p option to expose the container's port (e.g., 50923) to the host
    docker run --rm -it -p 50923:50923 gpt-academic
    ```

2.  ChatGPT + ChatGLM (Requires familiarity with Docker + understanding the Dockerfile + a powerful computer)
    ```sh
    # Modify the Dockerfile
    cd docs && nano Dockerfile+ChatGLM
    # Build (Dockerfile+ChatGLM is in the docs path, so `cd docs` first)
    docker build -t gpt-academic --network=host -f Dockerfile+ChatGLM .
    # Run (1) Directly:
    docker run --rm -it --net=host --gpus=all gpt-academic
    # Run (2) I want to enter the container to make some adjustments before running:
    docker run --rm -it --net=host --gpus=all gpt-academic bash
    ```

## Installation - Method 3: Other Deployment Methods (Requires cloud server knowledge and experience)

1.  Remote Cloud Server Deployment
    Please visit [Deployment Wiki-1](https://github.com/binary-husky/chatgpt_academic/wiki/%E4%BA%91%E6%9C%8D%E5%8A%A1%E5%99%A8%E8%BF%9C%E7%A8%8B%E9%83%A8%E7%BD%B2%E6%8C%87%E5%8D%97)

2.  Using WSL2 (Windows Subsystem for Linux)
    Please visit [Deployment Wiki-2](https://github.com/binary-husky/chatgpt_academic/wiki/%E4%BD%BF%E7%94%A8WSL2%EF%BC%88Windows-Subsystem-for-Linux-%E5%AD%90%E7%B3%BB%E7%BB%9F%EF%BC%89%E9%83%A8%E7%BD%B2)

3.  How to run under a subpath (e.g., `http://localhost/subpath`)
    Please visit [FastAPI Running Instructions](docs/WithFastapi.md)

## Installation - Proxy Configuration
1.  Standard Method
    [Configure Proxy](https://github.com/binary-husky/chatgpt_academic/issues/1)

2.  Beginner's Tutorial
    [Beginner's Tutorial](https://github.com/binary-husky/chatgpt_academic/wiki/%E4%BB%A3%E7%90%86%E8%BD%AF%E4%BB%B6%E9%97%AE%E9%A2%98%E7%9A%84%E6%96%B0%E6%89%8B%E8%A7%A3%E5%86%B3%E6%96%B9%E6%B3%95%EF%BC%88%E6%96%B9%E6%B3%95%E5%8F%AA%E9%80%82%E7%94%A8%E4%BA%8E%E6%96%B0%E6%89%8B%EF%BC%89)

---

## Customizing New Shortcut Buttons / Custom Function Plugins

1.  Customizing New Shortcut Buttons (Academic Shortcuts)
    Open `core_functional.py` with any text editor and add an entry as shown below, then restart the program. (If the button is already added and visible, the prefix and suffix support hot-reloading without needing a restart.)
    For example:
    ```python
    "Super English-to-Chinese": {
        # Prefix, added before your input. Used to describe your request, e.g., translate, explain code, polish, etc.
        "Prefix": "Please translate the following content into Chinese, then use a markdown table to explain the proper nouns that appear in the text one by one:\n\n",

        # Suffix, added after your input. For example, can be used with a prefix to wrap your input content in quotes.
        "Suffix": "",
    },
    ```
    <div align="center">
    <img src="https://user-images.githubusercontent.com/96192199/226899272-477c2134-ed71-4326-810c-29891fe4a508.png" width="500" >
    </div>

2.  Customizing Function Plugins

    Write powerful function plugins to perform any task you can imagine. The difficulty of writing and debugging plugins for this project is very low. As long as you have basic Python knowledge, you can follow the templates we provide to implement your own plugin functions. For details, please refer to the [Function Plugin Guide](https://github.com/binary-husky/chatgpt_academic/wiki/%E5%87%BD%E6%95%B0%E6%8F%92%E4%BB%B6%E6%8C%87%E5%8D%97).

---

## Partial Feature Showcase

1.  Image Display:
    <div align="center">
    <img src="https://user-images.githubusercontent.com/96192199/228737599-bf0a9d9c-1808-4f43-ae15-dfcc7af0f295.png" width="800" >
    </div>

2.  Self-Analysis of this Project's Code (When a program can read and analyze itself):
    <div align="center">
    <img src="https://user-images.githubusercontent.com/96192199/226936850-c77d7183-0749-4c1c-9875-fd4891842d0c.png" width="800" >
    </div>
    <div align="center">
    <img src="https://user-images.githubusercontent.com/96192199/226936618-9b487e4b-ab5b-4b6e-84c6-16942102e917.png" width="800" >
    </div>

3.  Analysis of Any Other Python/C++/Java/Go/React/... Project:
    <div align="center">
    <img src="https://user-images.githubusercontent.com/96192199/226935232-6b6a73ce-8900-4aee-93f9-733c7e6fef53.png" width="800" >
    </div>
    <div align="center">
    <img src="https://user-images.githubusercontent.com/96192199/226969067-968a27c1-1b9c-486b-8b81-ab2de8d3f88a.png" width="800" >
    </div>

4.  One-Click Reading Comprehension and Summary Generation for LaTeX Papers
    <div align="center">
    <img src="https://user-images.githubusercontent.com/96192199/227504406-86ab97cd-f208-41c3-8e4a-7000e51cf980.png" width="800" >
    </div>

5.  Automatic Report Generation
    <div align="center">
    <img src="https://user-images.githubusercontent.com/96192199/227503770-fe29ce2c-53fd-47b0-b0ff-93805f0c2ff4.png" height="300" >
    <img src="https://user-images.githubusercontent.com/96192199/227504617-7a497bb3-0a2a-4b50-9a8a-95ae60ea7afd.png" height="300" >
    <img src="https://user-images.githubusercontent.com/96192199/227504005-efeaefe0-b687-49d0-bf95-2d7b7e66c348.png" height="300" >
    </div>

6.  Modular Function Design
    <div align="center">
    <img src="https://user-images.githubusercontent.com/96192199/229288270-093643c1-0018-487a-81e6-1d7809b6e90f.png" height="400" >
    <img src="https://user-images.githubusercontent.com/96192199/227504931-19955f78-45cd-4d1c-adac-e71e50957915.png" height="400" >
    </div>

7.  Translate Source Code to English
    <div align="center">
    <img src="https://user-images.githubusercontent.com/96192199/229720562-fe6c3508-6142-4635-a83d-21eb3669baee.png" height="400" >
    </div>

8.  Online Information Aggregation from the Internet
    <div align="center">
    <img src="https://user-images.githubusercontent.com/96192199/233575247-fb00819e-6d1b-4bb7-bd54-1d7528f03dd9.png" width="800" >
    <img src="https://user-images.githubusercontent.com/96192199/233779501-5ce826f0-6cca-4d59-9e5f-b4eacb8cc15f.png" width="800" >
    </div>

## Todo & Version Plan:
-   version 3.3+ (todo): NewBing support
-   version 3.2: Function plugins support more parameter interfaces (save conversation function, analyze code in any language + query any combination of LLMs simultaneously)
-   version 3.1: Support querying multiple GPT models simultaneously! Support for api2d, support for multiple API key load balancing
-   version 3.0: Support for ChatGLM and other small LLMs
-   version 2.6: Refactored plugin structure, improved interactivity, added more plugins
-   version 2.5: Self-updating, solved the problem of text being too long and token overflow when summarizing large source code projects
-   version 2.4: (1) Added PDF full-text translation function; (2) Added function to switch the position of the input area; (3) Added vertical layout option; (4) Optimized multi-threaded function plugins.
-   version 2.3: Enhanced multi-threaded interactivity
-   version 2.2: Function plugins support hot-reloading
-   version 2.1: Collapsible layout
-   version 2.0: Introduced modular function plugins
-   version 1.0: Basic functions

ChatGPT Academic Developer QQ Group: 734063350

## References and Learning
```
The code references designs from many other excellent projects, mainly including:

# Reference Project 1: Adopted many techniques from ChuanhuChatGPT
https://github.com/GaiZhenbiao/ChuanhuChatGPT

# Reference Project 2: Tsinghua's ChatGLM-6B:
https://github.com/THUDM/ChatGLM-6B
```
