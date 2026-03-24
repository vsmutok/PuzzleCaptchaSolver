# Puzzle Captcha Solver 🧩🧩

PuzzleCaptchaSolver is a Python project designed to solve various puzzle CAPTCHAs such as Geetest3, Geetest4, Binance, DataDome, TikTok, and others. This project leverages OpenCV to process images and identify the position of the puzzle piece (slide) within the background image.

<!-- AD -->
---
## Sponsors

✅ CapMonster.Cloud — Fast, Reliable CAPTCHA Solving for Automation & Scraping

[![CapMonster Cloud](https://help.zennolab.com/upload/u/02/020538b7c128.png)](https://capmonster.cloud/en/?utm_source=github&utm_campaign=vsmutok_PuzzleCaptchaSolver)

If you are tired of wasting time solving endless CAPTCHAs during scraping, automation, or testing — we’ve got a solution for you.  
Meet CapMonster.Cloud — the AI-powered CAPTCHA solving service trusted by thousands of users worldwide. 🚀

--

🔥 **Why users love CapMonster.Cloud**
  
💡 Very high success rates (up to 99%)  
⚡ Super fast solving times  
💲 Affordable transparent pricing (pay per 1,000 CAPTCHAs)  
🔌 Easy integration via API + browser extensions  
⭐ Excellent reviews on TrustPilot, SourceForge, SaaSHub, AlternativeTo

--

🔗 **Useful Links**

💲 [Pricing & Supported CAPTCHA Types (25+ types supported)](https://capmonster.cloud/en?utm_source=github&utm_campaign=vsmutok_PuzzleCaptchaSolver#new-plans)  
📘 [API Documentation](https://docs.capmonster.cloud/?utm_source=github&utm_campaign=vsmutok_PuzzleCaptchaSolver)  
💡 Main Website → [capmonster.cloud](https://capmonster.cloud/en/?utm_source=github&utm_campaign=vsmutok_PuzzleCaptchaSolver)  
⭐ Reviews → [TrustPilot](https://www.trustpilot.com/review/capmonster.cloud)

---
<!-- /AD -->

## Features

- **Whitespace Removal:** Automatically crops the image to remove any unnecessary whitespace.
- **Edge Detection:** Highlights the edges of images to improve the accuracy of template matching.
- **Slide Positioning:** Accurately finds and marks the position of the puzzle piece within the background image.

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/vsmutok/Puzzle-Captcha-Solver.git
   cd Puzzle-Captcha-Solver
   ```
2. Create and activate virtual environment:
   ```sh
   python3 -m venv .venv
   source .venv/bin/activate
   ```
3. Install the required dependencies:
   ```sh
   pip install -r requirements.txt
   ```


## Usage

The primary class in this project is `PuzzleCaptchaSolver`. Here's how you can use it:

1. **Initialization:** Create an instance of `PuzzleCaptchaSolver` by providing the paths to the gap image, background image, and the output image path.

2. **Discern:** Call the `discern` method to process the images and find the position of the slide.

### Example

```python
from PuzzleCaptchaSolver import PuzzleCaptchaSolver

if __name__ == "__main__":
    solver = PuzzleCaptchaSolver(
        gap_image_path="demo/geetest4/1_slice.png",
        bg_image_path="demo/geetest4/1_bg.png",
        output_image_path="demo/geetest4/1_result.png"
    )
    position = solver.discern()
    print(f"The position of the slide is: {position}")
```

**Input Images**:
- Background Image
> ![Background Image](demo/geetest4/1_bg.png)
- Slide Image
>![Slide Image](demo/geetest4/1_slice.png)

**Output Image**:
> ![Result Image](demo/geetest4/1_result.png)

In the resulting image, the detected position of the sliding piece is highlighted with a red rectangle.


### Methods

- `remove_whitespace(image)`: Removes whitespace from an image.
- `apply_edge_detection(img)`: Applies edge detection on the given image.
- `find_position_of_slide(slide_pic, background_pic)`: Finds the position of the slide on the background picture.
- `discern()`: Performs the full discernment process to find the position of the slide in the given images.

## Contributing

Contributions are welcome! If you have any suggestions, feel free to open an issue or create a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Acknowledgements

- [OpenCV](https://opencv.org/) for their powerful image processing library.

---

By using this project, you can efficiently solve various puzzle CAPTCHAs, making it easier to automate interactions with websites that use these types of verifications.

___
#### Disclaimer
_This repository is created for informational purposes only. I do not advise or condone violating the policies of any website._

___
⭐️ If you found this project helpful, please give it a star on GitHub!
