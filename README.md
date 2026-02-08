<p align="center">
  <img src="https://github.com/CorvaeOboro/sd_project_tools/blob/main/docs/sd_project_tools_header_long.png?raw=true" height="120" /> 
</p>

# diffusion_project_tools
- a collection of tools for interacting with image synthesis projects , organizing , reviewing , and generating . 

| review | comfy | prompt | video | audio | 
| :---: | :---: | :---: | :---: | :---: |
| <a href="https://github.com/CorvaeOboro/sd_project_tools#review-and-rank"> <img src="https://github.com/CorvaeOboro/sd_project_tools/blob/main/docs/thumb_image.png?raw=true" width="140" height="140" /> </a>| <a href="https://github.com/CorvaeOboro/sd_project_tools#comfyui-custom-nodes"> <img src="https://github.com/CorvaeOboro/sd_project_tools/blob/main/docs/thumb_comfy.png?raw=true" width="140" height="140" />  </a>  |  <a href="https://github.com/CorvaeOboro/sd_project_tools#prompt-entry"> <img src="https://github.com/CorvaeOboro/sd_project_tools/blob/main/docs/thumb_prompt.png?raw=true" width="140" height="140" />  </a>  | <a href="https://github.com/CorvaeOboro/sd_project_tools#video-tools"> <img src="https://github.com/CorvaeOboro/sd_project_tools/blob/main/docs/thumb_video.png?raw=true" width="140" height="140" />  </a>  | <a href="https://github.com/CorvaeOboro/sd_project_tools#voice-action-tools"> <img src="https://github.com/CorvaeOboro/sd_project_tools/blob/main/docs/thumb_voice.png?raw=true" width="140" height="140" /> </a>|

# install
- install python 3.10
- [download diffusion_project_tools](https://github.com/CorvaeOboro/sd_project_tools/archive/refs/heads/master.zip) and extract to a folder
- quick install using [00_install_and_launch.bat](https://github.com/CorvaeOboro/sd_project_tools/blob/main/00_install_and_launch.bat) = it creates an isolated local Python virtual environment and installs the [requirements.txt](https://github.com/CorvaeOboro/sd_project_tools/blob/main/requirements.txt) into it , then runs launcher tool ui to  launch any of the project tools shown below .

or manually install:
- create a virtual environment: `python -m venv venv`
- activate the virtual environment:
    - Windows: `venv\Scripts\activate`
    - macOS/Linux: `source venv/bin/activate`
- install requirements: `pip install -r requirements.txt`
- run [launch_tools.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/launch_tools.py)

# Launcher
<img src="https://github.com/CorvaeOboro/sd_project_tools/blob/main/docs/launch_tools.png?raw=true" />

- [launch_tools.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/launch_tools.py) = Central launcher UI for all project tools 

# Review and Rank
- [image_review_and_rank_multi_project.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/image_review_and_rank_multi_project.py) = project image reviewer , quickly rank images into subfolders using left click = 1 and right click = 2 , colorizes by amount 
 <a href="https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/image_review_and_rank_multi_project.py"> <img src="https://github.com/CorvaeOboro/sd_project_tools/blob/main//docs/image_review_and_rank_multi_project.png?raw=true" height="300" /> </a>
- [image_review_and_rank.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/image_review_and_rank.py) = simpler image viewer from a folderpath , quickly rank fullscreen singular images into subfolders using 1,2, or 3 . navigate with arrows . view as tiled texture with T 

# Tensor Info and Sorting
<img src="https://github.com/CorvaeOboro/sd_project_tools/blob/main//docs/tensor_tools_all.png?raw=true" height="200" /> 

- [tensor_tools_all.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/tensor_tools_all.py) = gets info from civitai , sorts by info by model type and category , removes duplicates by hash
- [lora_project_structure_generator.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/lora_project_structure_generator.py) = generates project folder structures from LoRA .info files with automatic image downloads and prompt extraction to /prompt/prompt_flux.md

# Prompt Entry
<a href="https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/gen_project_prompt_entry.py"> <img src="https://github.com/CorvaeOboro/sd_project_tools/blob/main//docs/gen_project_prompt_entry.png?raw=true" height="200" /> </a>

- [gen_project_prompt_entry.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/gen_project_prompt_entry.py) = GUI dashboard for managing multiple item prompts , support for SDXL and SD1.5 positive/negative prompts and FLUX and VIDEO prompts
- [project_status_dashboard.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/project_status_dashboard.py) = dashboard to visualize and track project generation status and outputs

# Image Tools
- [image_editor_layered.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/image_editor_layered.py) = basic GUI tool to edit an image with multiple layers
- [image_text_prompt_tools.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/image_text_prompt_tools.py) = GUI tool to drag drop image and for prompt management. merge multiple prompts without duplicates, balance prompt strengths, simplify prompt structure (remove parentheses), scale LoRA strengths to target maximum, 
- [lora_variants.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/lora_variants.py) = input a prompt with loras and generate all permutations of strengths , within a range of total lora strength and per lora strengths . the output can then be used for x/y plot or as wildcard
- [lora_previews_to_list.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/lora_previews_to_list.py) = given a folder of lora previews creates a list
 - [image_icon_generator.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/image_icon_generator.py) = generate app icons/thumbnails from images with safe padding and backgrounds
 - [image_inspect_bmp.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/image_inspect_bmp.py) = inspect BMP headers and pixel data for debugging/validation
 - [image_metadata_badword_scanner.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/image_metadata_badword_scanner.py) = scan image metadata/captions for bad words and produce a cleaned report
 - [image_psd_reconstruct.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/image_psd_reconstruct.py) = reconstruct images from PSD layers for analysis or export

- # Video Tools
- [video_clip_marker.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/video_clip_marker.py) = tool for marking and processing video clips
- <img src="https://github.com/CorvaeOboro/sd_project_tools/blob/main/docs/video_clip_marker.png?raw=true" height="300" />
- [video_combine.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/video_combine.py) = GUI tool for combining videos, adjusting speed, removing first frames, and batch processing video folders. Uses ffmpeg
- [video_add_audio.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/video_add_audio.py) = quick Add audio to a video file using ffmpeg and ffprobe. Supports both GUI and CLI modes. Drag-and-drop interface.
- [video_place_in_image_composite.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/video_place_in_image_composite.py) = GUI tool to composite a video into a region of an image using template matching and homography. 
- [video_webp_pingpong.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/video_webp_pingpong.py) = creates ping-pong WebP animations from video files
- [video_psd_to_timelapse_anim.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/video_psd_to_timelapse_anim.py) = Converts PSD layers to timelapse animations, UI and CLI, exports to video gif or webp or webm. updated to use [image_psd_to_timelapse_export.jsx](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/image_psd_to_timelapse_export.jsx) a photoshop javascript to do the exporting faster 
<img src="https://github.com/CorvaeOboro/sd_project_tools/blob/main/docs/image_psd_to_timelapse_anim.png?raw=true" height="200" />

- [video_editor_word_rating.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/video_editor_word_rating.py) = GUI tool to rate video frames using words 
- [video_review_and_rank_multi_project.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/video_review_and_rank_multi_project.py) =UI for reviewing and ranking video files
 - [VIDEO_cursor_removal.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/VIDEO_cursor_removal.py) = detect and remove mouse cursor overlays from screen recordings
 - [VIDEO_image_sequence_to_webp.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/VIDEO_image_sequence_to_webp.py) = convert folders of image sequences into optimized animated WebP
 - [video_audio_batch_processor.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/video_audio_batch_processor.py) = batch operations for extracting, replacing, or adjusting audio across many videos
 - [video_interlacing_fix.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/video_interlacing_fix.py) = deinterlace and repair interlaced footage using ffmpeg filters
 - [video_to_gif_cropper.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/video_to_gif_cropper.py) = crop and clip video into looping GIF or WebP
  - [video_music_sync.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/video_music_sync.py) = align audio to music video timing via waveform analysis , useful for syncing stage show to record audio
  <img src="https://github.com/CorvaeOboro/sd_project_tools/blob/main/docs/video_music_sync.png?raw=true" height="400" />

# Voice Action Tools
- [voice_action_organizer.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/voice_action_organizer.py) = use voice to move selected files into specific folders , if nothing selected will open ot that location , useful for project organization . Requires the [Vosk speech model](https://alphacephei.com/vosk/models) for local offline speech recognition 
- <img src="https://github.com/CorvaeOboro/sd_project_tools/blob/main/docs/voice_action_organizer.png?raw=true" height="200" />

# Audio Tools
- [audio_timing_beat.py](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/audio_timing_beat.py) = analyze audio beat timing and markers for synchronization tasks

# comfyui custom nodes
workflow and custom nodes may be installed in the ComfyUI Manager or manually download and see node examples =
- [illumorae custom nodes](https://github.com/CorvaeOboro/comfyui_illumorae/)

# auto1111 project workflow
- archived tools built around the previous auto1111 workflow are in [/tools/archive/](https://github.com/CorvaeOboro/sd_project_tools/blob/main/tools/archive/) folder 
- this workflow is now recreated in comfyui using the projects [custom nodes](https://github.com/CorvaeOboro/comfyui_illumorae/)

# LICENSE
- free to all , [creative commons zero CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) , free to re-distribute , attribution not required