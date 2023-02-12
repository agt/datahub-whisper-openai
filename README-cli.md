
# Whisper CLI demos

## Prepare environment

Install openai-whisper: 
- `!pip show -qq openai-whisper || pip install --user git+https://github.com/openai/whisper.git`

_Note: this step duplicates setup performed in WhisperDemo.ipynb, so may not be needed._

Configure Bash command search path:
- `echo 'export PATH=~/.local/bin:$PATH' >> ~/.bash_profile && . ~/.bash_profile`

## Transcription examples

- `whisper --output_format txt --task transcribe --language en Winston_Churchill_-_Be_Ye_Men_of_Valour.wav`
- `whisper --output_format txt --task transcribe --language en khosla.wav`

## Monitoring GPU usage during execution

In a separate terminal window, run:

- `watch -n 1 nvidia-smi`

You'll see the model being uploaded to GPU ram followed by GPU core activity as it's executed.