# google-translate-text-to-sppech
import os
from gtts import gTTS
from googletrans import Translator, constants
from pprint import pprint
from translate import Translator
translator= Translator(from_lang="hindi",to_lang="english")
translation = translator.translate("क्या हाल है?")
print(translation)


myText=translation
language="en"
output=gTTS(text=myText,lang=language,slow=False)
output.save("output.mp3")
os.system("start output.mp3")
