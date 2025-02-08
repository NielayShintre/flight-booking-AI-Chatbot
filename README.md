# FlightAI Chatbot

This project implements a simulated flight booking chatbot using OpenAI's API, with additional support for text-to-speech, image generation, and a dummy booking system.

## Features
- **Conversational AI:** Uses OpenAI's chat API to interact with users.
- **Tool Calls:** Handles external tool calls for fetching ticket prices and generating vacation images.
- **Image Generation:** Creates a pop-art-style vacation image using OpenAI's DALL·E API.
- **Text-to-Speech:** Converts chatbot responses into audio using OpenAI's TTS API.
- **Simulated Booking:** Confirms flight bookings as a dummy process, responding with departure and return details.

## Installation
1. Install dependencies:
   ```sh
   pip install openai pydub pillow gradio
   ```
2. Install FFmpeg (required for `pydub` audio playback):
   ```sh
   brew install ffmpeg  # macOS
   sudo apt install ffmpeg  # Linux
   ```

## Usage
Import the chatbot module and initiate a conversation:
```python
history, image = chat(history=[], to_date="2025-03-10", return_date="2025-03-20", prev_image=None)
```

## Functions Overview
### `chat(history, to_date, return_date, prev_image)`
Handles user interactions, generates responses, and simulates a booking if confirmed.

### `simulate_booking(city, to_date, return_date)`
Returns a dummy confirmation message with the booking details.

### `artist(city)`
Generates a vacation-themed image for the given city.

### `talker(message)`
Converts chatbot responses into speech and plays the audio.

## Notes
- The chatbot does **not** perform real bookings; it only simulates the experience.
- Ensure your OpenAI API key is properly configured in your environment.

## License
This project is for educational and demonstration purposes only.

