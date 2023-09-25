## Accident Detection System using YOLOv8 and Raspberry Pi

Our project leverages the power of YOLOv8 and Raspberry Pi to create an Accident Detection System. It's designed to promptly identify accidents, categorizing them as 'moderate' or 'severe,' and immediately notify authorities through email and WhatsApp using Twilio integration. With the added visual cue of an RGB LED, this system enhances situational awareness, making it invaluable for remote area accident monitoring through IP camera live streams.

### Step 1: Setup

- Create a virtual environment and activate it: `python -m venv venv && source venv/bin/activate`
- Install Prerequisites: `pip install -r requirements.txt`
- Clone this repository: `git clone https://github.com/kir4nn/AccidentDetectionYolov8.git`
- `cd` into the directory: `cd AccidentDetectionYolov8`, then proceed to Step 2

### Step 2: Detection

#### Step 2.1: Static Image/Video Detection

- To perform static image/video detection, use the file named `detecting_static.py` available in `ML` folder
- Run the script: `python detecting_static.py`
- The script will load the model, perform object detection on the specified image (sample input images available in sample input folder), and save the results in the `results` directory.

#### Step 2.2: Videostream Detection

- To perform videostream detection, use the file named `detecting_videostream.py` available in `ML` folder
- Run the script: `python detecting_videostream.py`
- The script will load the model, perform object detection on the input videostream (specified by the `stream_url`) by converting it to individual frames.
