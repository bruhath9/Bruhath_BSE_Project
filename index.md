R

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Bruhath B | Lynbrook High School | Computer Engineering | Incoming Senior

<img src="bruheadshot.JPG" alt="Description" width="300">
  
# Final Milestone


# Second Milestone

For my second milestone, I set up the object recognition algorithm using a machine learning framework called TensorFlow, which I installed on the Raspberry Pi. With TensorFlow, when I point the camera at an object--such as a laptop, coffee mug, or telephone--a label appears on the screen identifying what the object is in real time as a demo. The model I used is a pre-trained one called MobileNetV2, developed by Google. Since it's pre-trained, it has already been exposed to thousands of images of around 80 to 100 common objects and has learned to recognize their unique patterns and features. These include everyday items like a keyboard, mouse, phone, and more.

Additionally, in order to integrate the camera into the project, I designed and 3D-printed a simple mount that attaches directly to the glasses. The camera is secured to the mount with screws, and the mount is attached to the glasses using hot glue. One of the challenges I faced was dealing with camera errors while running the object recognition algorithm. I accidentally damaged the camera by handling it improperly and had to replace it. Another hurdle was figuring out how to mount the camera to the glasses securely. After experimenting with tape and the default camera case, I decided that designing a custom 3D-printed mount was the best solution.


# First Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/aelxbT13E-M?si=j0CjPNI0-CN-dHPi" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

For my first milestone, I set up my Raspberry Pi by displaying it to my laptop via a software called TigerVNC which allows me to remotely stream the pi to my laptop screen to see what's going on on the raspberry pi's UI. I also did a headless setup called SSH (secure shell) which allows me to remotely run commands on my raspberry pi and essentially make it do things such as taking a photo all through VS Code without requiring a display on a monitor of the pi. To do this, my laptop and the raspberry pi have to be on the same network, and remotely programming the pi requires specifying which port to use on VS Code so that we can reach the pi's SSH server.

Additionally, I set up the photo-taking feature of the Raspberry Pi through a couple of lines of code which used Python's Picamera2 library which allows me to access the built-in camera feature of the Pi and take a photo upon running the software. The camera used is a special Raspberry Pi camera module which is attached to the Pi through a ribbon-like cable/wire. OpenCV, which is a real-time computer vision and machine learning software, had to be donwloaded in order to save the image taken by the camera onto an SD card which is also attached to the Pi.

![Headstone Image](IMG_4518.JPG)

# Starter Project: Retro Arcade Game

<iframe width="560" height="315" src="https://www.youtube.com/embed/z90Ao1cDq40?si=WT4S7g19cpYrOn5E" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

I chose to complete the Retro Arcade Game for my starter project because I thought that building a game device which I could play on my own time was pretty cool. Additionally, as stated in the video, I thought that the Retro Arcade Game would be a rather intriciate/difficult project to start with, and is great practice for my soldering technique as there were many parts that had to be properly soldered and in tight spaces as well. The arcade game has multiple pre-coded games such as Tetris and Snake and here's how it works:

- Multiple components such as buttons (directions, on/off, gamemode change), a buzzer, a score display, the game board, a USB-mini socket (for power), and a battery pack are all soldered onto a PCB.
- The PCB has an STC microprocessor which processes input from all the buttons when pressed, and also stores and runs code which contains the different games mentioned above.
- The button actions are processed by the microprocessor through copper traces that are printed on the PCB; the button completes the current that is passing through the resistor and the battery, and when the current is completed, a signal is sent to the microprocessor to complete in action, which can be as simple as scrolling through the games, or rotating a piece in Tetris.

# Schematics 
![Headstone Image](tinkermount.JPG)

Above is the simple design for the camera mount to the glasses.


# Code
Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. 

```c++
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  Serial.println("Hello World!");
}

void loop() {
  // put your main code here, to run repeatedly:

}
```

# Bill of Materials

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Raspberry Pi 4 Kit | Computer that handles image processing and system control for the glasses| $119.95 | <a href="https://www.canakit.com/raspberry-pi-4-starter-kit.html"> Link </a> |
| Raspberry Pi Camera Module | Captures images to be input into the Raspberry Pi | $9.99 | <a href="https://www.amazon.com/Arducam-Raspberry-Camera-Module-1080P/dp/B07RWCGX5K/ref=asc_df_B07RWCGX5K?mcid=ac983c0aeb843492a7f6d48d54a3e05a&hvocijid=1425345951002749708-B07RWCGX5K-&hvexpln=73&tag=hyprod-20&linkCode=df0&hvadid=721245378154&hvpos=&hvnetw=g&hvrand=1425345951002749708&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9032183&hvtargid=pla-2281435178818&th=1"> Link </a> |
| Earbuds | To listen to text to speech function of Raspberry Pi| $19.99 | <a href="https://www.amazon.com/Sony-MDREX15AP-B-Black/dp/B00JG2WRUO/ref=sr_1_3?crid=1GY75F91PMUGL&dib=eyJ2IjoiMSJ9.5AA1u0LZHgM78VUfUdqXE8_s2i5C-4lV7r3H_Zrt-XphwuiYe-HNQc_s0n0XzAawd1JpSrMKTfAPiP1jzHESdNhuY33xLIq9LKW1Fz7wZ9RkhTnOIuiTYLVpymTe-RaSxlEaA4Nf5VeBybh2sd1tji_p4Y58_zxgToQFWwjw54gUdQaBlOrNIbavIH1eNfRgHnWGOw4nw8LqdWEfeFRUTR53CVkga6arVhbNaD1LWCFOI5pvx9MtBEW_NPtjmhVQGBRwDNrLZjAKUOH-6o7xmYm8cWN7UXpJr9GRQ8ypJFw.MmFlPFDOuN7sekiKeKlalFsO1XA6bRxG7x0BVjFBspE&dib_tag=se&keywords=sony%2Bearbuds&qid=1751488791&s=electronics&sprefix=sony%2Berabu%2Celectronics%2C180&sr=1-3&th=1"> Link </a> |
| Clear glasses | Main glasses upon which camera is mounted| $6.59 | <a href="https://www.amazon.com/Glasses-Bluelight-Womens-Blocking-Gaming/dp/B0D47J1P9L/ref=sr_1_4?crid=2U3JX46PP1YQ5&dib=eyJ2IjoiMSJ9.rK2Oq1Z75QQhRq6f0QUoxqu4RsrvvN4-7uOkvUycMizXug5d4rAzL0z5PYOZFd_ZxeiS3fj5JgF00Towo1kwJ_NzLM2nu5C2rMZ3tbi_u94h5O5WOaiHfNMs3VvmwcqPp183FNb-nwuow9nJbUC1Jq211HxtHQXrS8O5Hqn4j9k0EUB6_3Lnv1LlQQbhrrLfn6WayrraOMVG-r3ejjSLZopIFf8Hu40h-MDKOgiEx2LG0YobFUMAlZZdmM_CsmwBDZWsi2Q2pWGLhHNNl0zK2WscFNvbiXytO5p3skOWIgo.-60dL36sVlGRKSMy3k-XOQvnLa_vUMN-R1Vk1S5eDrg&dib_tag=se&keywords=clear%2Bbluelight%2Bglasses&qid=1751488889&s=electronics&sprefix=clear%2Bbluelight%2Bglasses%2Celectronics%2C221&sr=1-4&th=1"> Link </a> |
| Power bank | Mobile power source for Raspberry Pi| $21.99 | <a href="https://www.amazon.com/INIU-High-Speed-Flashlight-Powerbank-Compatible/dp/B07CZDXDG8/ref=sr_1_3?crid=53URT6OP6FHU&dib=eyJ2IjoiMSJ9.QKGsYnUA7w9IYsHtGbbDBqIPNqk72m127EvLDj4h4xbK4PihUjQsjylRthVPXKduCEGzyUpg7f3q0NPty07_-KFT7T5qr__K57D5hRdcXoHELBfMdok_E_9y1Df1063YsnHjxpRKS_a398z0ONZphacjUTxCOIzKHFdBBrsFpfkb790Sw_pyPRSDa7rArLGqoH6P9PGsHUxtRCI7lsx3nkImJOaF1GeY9Apk7IPch8754krUzQFSrwshZ8RLcLZSVmf0nZDSr6gLtz1VABsNEapXiItDG5V8GMGgI8JPnDk.IsEEt-fYtmCt4CweTWkltJF8zsH_XhjGRX3EqgUwA7A&dib_tag=se&keywords=iniu%2Bpower%2Bbank&qid=1751488984&s=electronics&sprefix=iniu%2Bpower%2Bba%2Celectronics%2C370&sr=1-3&th=1"> Link </a> |
| HDMI Video Capture Card | To interact with Raspberry Pi UI on external monitor| $9.98 | <a href="https://www.amazon.com/Audio-Express-AXHDCAP-Broadcasting-Conference/dp/B0C2MDTY8P/ref=sr_1_3?crid=2BX43CAYPODYE&dib=eyJ2IjoiMSJ9.jqv_PPTyMd5Yw9Wlfle7WftEF62bGg5qpcOk2xxrMPt2e4ZaBTNSBKUvKtLs6u3XEsd8GOnOALOi5SmrKqx_Twh0IGnbvwjg8xxyFuOfBoOuWCn4SmQPPg7--XyFTzopqrZ2sDhggg-bG-HP1zU6PxAzcCMx6LCSos0grBFNFvNZGRiw5zstmF16TSbhjujUgW5Cfy55zxO4Lxlq6XhzFxzqOvQJ5xltH-ki3b5qm0DckQHTlDXYzFt4fq02lei5UGEBSp-Whti9gAz7Z3qbUEqcsv_3dgxv4zsxz1n7Ck8.rfTcXMY_ExQTQji5B6Zh7YL4levLc6MyTa2Bm3rt7Bg&dib_tag=se&keywords=hdmi+video+capture+card&qid=1751489136&s=electronics&sprefix=hdmi+video+capture+car%2Celectronics%2C190&sr=1-3"> Link </a> |

# Other Resources/Examples

