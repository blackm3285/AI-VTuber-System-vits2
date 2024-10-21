# AI-VTuber-System
Replaced OpenAI TTS to local Bert-VITS2-2.3

You can edit vits api prompt in ./TextToSpeech/OpenAITTS.py

```
# Updated openaitts function using Gradio Client instead of OpenAI API
def openaitts(
        text="",
        output_path="Audio/output_openaitts_01.wav",
        model="tts-1",    # Kept in function signature, not used
        voice="alloy",    # Kept in function signature, not used
        speed=1.00,       # Kept in function signature, not used
        format="wav",     # Kept in function signature, not used
        timeout=10.0,     # Kept in function signature, not used
        speaker="Your_Speaker",    # Default speaker
        sdp_ratio=0.5,      # Default SDP Ratio
        noise_scale=0.5,    # Default Noise
        noise_scale_w=0.9,  # Default Noise_W
        length_scale=1.0,   # Default Length scale
        language="auto",      # Default Language
        audio_prompt=None,          # Path for audio prompt (optional)
        text_prompt="",        # Default text prompt for style
        prompt_mode="Text prompt",  # Default prompt mode
        style_text="",      # Auxiliary text for style (optional)
        style_weight=0.7,   # Weight of the auxiliary text (optional)
        ):

    try:
        # Gradio Client initialization
        client = Client("http://127.0.0.1:7860/")
```
