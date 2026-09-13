<img width="546" height="102" alt="kanarenshu" src="https://github.com/user-attachments/assets/866defe1-75f0-446c-a9c5-44e00fb98522" />

# Kana Renshū（。＾▽＾）🌸
Welcome to the repository of Kana Renshū!

### What is Kana Renshū? 
- Kana Renshū is a Japanase Kana (Hiragana) trainer program, you can practice your skills in Japanese characters!
- Dakuten, and Handakuten characters are supported!
- *Katakana newly installed.*

<img width="418" height="153" alt="Képernyőkép 2026-09-13 113538" src="https://github.com/user-attachments/assets/f7d4cb98-88f6-4d6e-8e55-59e62f65db56" />
<img width="417" height="154" alt="Képernyőkép 2026-09-13 113528" src="https://github.com/user-attachments/assets/e6c23125-9901-4b8d-bdb4-be54645913b4" />

**Hiragana Characters:** 
> hiragana_chart = "あいうえおかがきぎくぐけげこごさざしじすずせぜそぞただちぢつづてでとどなにぬねのはばぱひびぴふぶぷへべぺほぼぽまみむめもゃやゅゆょよらりるれろゎわゐゑをんゔゕゖゝゞ"

**Katakana Characters:** 
> katakana_chart = 'アイウエオカガキギクグケゲコゴサザシジスズセゼソゾタダチヂツヅテデトドナニヌネノハバパヒビピフブプヘベペホボポマミムメモヤユヨラリルレロワヰヱヲンヴヷヸヹヺ"
### How to use it? 
The program displays a Hiragana character, and then you need to write it in romaji.
There will be an input field, that's where you need to write the answear, then hit the check button.

### About the Code
It's simple, and I made mistakes in the UI, so please forgive me...
```
#Loading the banner, and starts displaying the interface.
        current_path = os.path.dirname(os.path.realpath(__file__))
        self.bg_image = customtkinter.CTkImage(Image.open(current_path + "\\banner.png"),
                                               size=(self.width, self.height))
        self.bg_image_label = customtkinter.CTkLabel(self, image=self.bg_image)
        self.bg_image_label.grid(row=0, column=0)
        self.text_label = customtkinter.CTkButton(self, font=("Arial", 55, 'bold'), text_color='#202020', text=selectedChar, width=370, height=50, fg_color=("#46ec67", "#46ec67"))
        self.text_label.grid(row=0, column=0, padx=30, pady=(0, 45))
        self.check_button = customtkinter.CTkButton(self, font=("Arial", 10, 'bold'), text_color='#202020', text="Check ✔", width=370, height=10, fg_color=("#46ec67", "#46ec67"), command=self.checkUserInput)
        self.check_button.grid(row=0, column=0, padx=30, pady=(46, 0))
        self.username_entry = customtkinter.CTkEntry(self, justify='center', text_color='#46ec67', font=("Arial", 13, 'bold'),  width=370, height=29, placeholder_text="Type the character in romaji: ")
        self.username_entry.grid(row=0, column=0, padx=30, pady=(98, 1))
    
```

> This project has been made in 2 days at a University, so it's not a big deal, use it as you please.

# If you want to build the code with PyInstaller module: 🏡
The code can be build on Windows and Linux too, but you need to use the --add-data subcommand for customtkinter .json.
If PyInstaller can't find the path bellow, use this command: ```pip show customtkinter, then at the end type \customtkinter;customtkinter!```
Do the same with pykakasi! ```pip show pykakasi, then at the end of the directory just change it to \pykakasi;pykakasi!```
### Windows: (≧∇≦)ﾉ
> python -m PyInstaller --noconfirm --onedir --windowed --add-data "C:\Users\ !! YOUR USERNAME HERE !!\AppData\Local\Packages\PythonSoftwareFoundation.Python.3.11_qbz5n2kfra8p0\LocalCache\local-packages\Python311\site-packages\customtkinter;customtkinter" --add-data "C:\Users\ !! YOUR USERNAME HERE !!\AppData\Local\Packages\PythonSoftwareFoundation.Python.3.11_qbz5n2kfra8p0\LocalCache\local-packages\Python311\site-packages\pykakasi;pykakasi" --icon=Icon.ico --noconsole KanaRenshu.py
```READ! THE BUILD FOLDER MUST CONTAIN THE BANNER.PNG IMAGE FILE, ELSE THE PROGRAM WILL CRASH!!!```
