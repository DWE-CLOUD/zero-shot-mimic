
# Instructions
- Run the below to start your instance -- you must run the Installation steps above first
```sh
# docker run --gpus=all -p 7860:7860 -it voicecrafter
```
- Visit the gradio.live link provided in the output or the local link provided -- commonly [localhost:7860](http://localhost:7860)

  **Note**: not currently authenticated so anyone with the link can use it
- Click the "Original Audio" tile to upload clear audio of only the subject speaking on the order of 5-10 seconds.

  **Tip**: Trim out anything longer and choose audio with no background noise or crackles and pops (file formats: mp3, m4a, wav)
- Update the "original_transcript" with the transcript of the audio uploaded or leave the Autotranscribe input checkbox checked if you want whisper to detect the text
- Update "target_transcript" with the sentence or two of text you want to generate
- Click "Run" to generate audio
- Click the play button next to "Generated Audio" to hear the clip and the "..." to download

# Models
| Model    | Parameters | Memory | Runs on |
| -------- | ------- | ------- | ------- |
| fast-whisper  |   |   | CPU |
| voicecraft | 330M     | 4GB+ VRAM | GPU |
| voicecraft    | 830M    | 6GB+ VRAM | GPU |


# Original VoiceCraft License
The codebase is under CC BY-NC-SA 4.0 (LICENSE-CODE), and the model weights are under Coqui Public Model License 1.0.0 (LICENSE-MODEL). Note that we use some of the code from other repository that are under different licenses: ./models/codebooks_patterns.py is under MIT license; ./models/modules, ./steps/optim.py, data/tokenizer.py are under Apache License, Version 2.0; the phonemizer we used is under GNU 3.0 License.

Please refer to the below for latest:
- [LICENSE-CODE](https://github.com/jasonppy/VoiceCraft/blob/master/LICENSE-CODE)
- [LICENSE-MODEL](https://github.com/jasonppy/VoiceCraft/blob/master/LICENSE-MODEL)
