### Google - Bard API
Use Python call, Bard API


[https://github.com/ttpho/Bard-API](https://ttpho.github.io/2023-11-25-bard/)


### Ask

```python

from bardapi import BardCookies
import sys

cookie_dict = {
    "__Secure-1PSIDTS": "xxxxxxxx",
    "__Secure-1PSID": "xxxxxxxx."
}

print("Ask anything: ")
input_text = str(input())
bard = BardCookies(cookie_dict=cookie_dict)
answer = bard.get_answer(input_text)
content_answer = answer['content']
print(content_answer)

```


### Text To Speech(TTS)

```python

from bardapi import BardCookies
import sys

cookie_dict = {
    "__Secure-1PSIDTS": "xxxxxx",
    "__Secure-1PSID": "xxxx."
}

print("Input text to speech")
input_text = str(input())
bard = BardCookies(cookie_dict=cookie_dict)
audio = bard.speech(input_text)
with open("speech.ogg", "wb") as f:
  f.write(bytes(audio['audio']))

```
