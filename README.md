# nlp4sleep
A rule-based NLP algorithm to identify sleep-related concepts from clinical notes using the OHNLP MedTagger framework.

## Definition of Sleep Concepts
|Concept Category|	Definition|	Example|
| --- | --- | --- |
|Snoring |	Snoring or snoring synonyms|	“snoring” “sleep apnea”|
|Napping |	Napping during daytime|	“napping” “doze”|
|Sleep problem |	Sleep problem, Specific sleep disorder/ condition/disease mentioned in the note|	“sleep disorder”, “insomnia”, “hypersomnia”|
|Bad sleep quality |	Any mention related to bad sleep quality in the note|	“sleeplessness” “couldn’t sleep during night” “staying up all night”|
|Daytime sleepiness |	Sleepiness during daytime|	“sleep a lot through out the day” “excessive daytime sleepiness”|
|Night wakings |	Night time wakings|	“frequent night waking” “waking up in the middle” “waking up 3-5 times”|
|Sleep duration (Short <=6h, Medium 6-8h, or Long >=8h)|	Duration of night time sleep|	“sleeps 4-5 hours” --> Short “sleep more than 12 hours” --> Long|

## Getting Started

### Installation and Use of MedTagger
#### Video demo: https://vimeo.com/392331446

1. Download the latest release from https://github.com/OHNLP/MedTagger/releases
2. Extract the zip file
3. Modify the `INPUTDIR`, `OUTPUTDIR`, and `RULEDIR` variables in `run_medtagger_win.bat` or `run_medtagger_unix_mac.sh`, as appropriate
    - `INPUT_DIR`: full directory path of input folder 
    - `OUTPUT_DIR`: full directory path of output folder
    - `RULES_DIR`: full directory path of 'Rule' folder
    
    Example for Mac:
    ```
    INPUTDIR="$YOUR_INPUT_DIRECTORY"
    OUTPUTDIR="$YOUR_OUTPUT_DIRECTORY"
    RULEDIR="$YOUR_MEDTAGGER_HOME/medtaggerieresources/covid19"
    ```
    
    Example for Windows:
    ```
    INPUTDIR="C:\$YOUR_INPUT_DIRECTORY\input"
    OUTPUTDIR="C:\$YOUR_OUTPUT_DIRECTORY\output"
    RULEDIR="C:\YOUR_MEDTAGGER_HOME\medtaggerieresources\covid19"
    ```
    
4. Run the batch file

    Mac/linux: 
    ```
    run_medtagger_unix_mac.sh
    ```
    
    Windows: 
    
    ```
    run_medtagger_win.bat
    ```
    


## Citation
Mohammad H, Sivarajkumar S, Viggiano S, Visweswaran S, Wang Y. Sleep Information Extraction from Clinical Notes of Patients with Alzheimer’s Disease Using Natural Language Processing. 2022.
