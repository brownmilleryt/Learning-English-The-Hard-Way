import random
from deep_translator import GoogleTranslator


tekst = "In the 1870s, newspapers and printers faced a very specific and very costly problem. Photography was a new and exciting medium at the time. Readers wanted to see more pictures, but nobody could figure out how to print images quickly and cheaply. For example, if a newspaper wanted to print an image in the 1870s, they had to commission an engraver to etch a copy of the photograph onto a steel plate by hand. These plates were used to press the image onto the page, but they often broke after just a few uses. This process of photoengraving, you can imagine, was remarkably time consuming and expensive. The man who invented a solution to this problem was named Frederic Eugene Ives. He went on to become a trailblazer in the field of photography and held over 70 patents by the end of his career. His story of creativity and innovation, which I will share now, is a useful case study for understanding the 5 key steps of the creative process."

def splitting_words(txt:str, split_by:str):
    txt = [i.strip() for i in txt.split(split_by)]
    while("" in txt):
        txt.remove("")
    return txt

teksty = splitting_words(tekst,".")

def replace_str(text_list:list):
    choose_text = random.choice(text_list)
    raw_txt = choose_text
    if len(choose_text) > 2:
        replacment = choose_text[0] + "_" * (len(choose_text) - 1)
    else:
        replacment = "_" * len(choose_text)
    return [choose_text,replacment,raw_txt]

x = random.choice(teksty)
y = replace_str(splitting_words(x," "))
z = x.replace(y[0], y[1],1)

translated = GoogleTranslator(source='en', target='pl').translate(x)
translatedw = GoogleTranslator(source='en', target='pl').translate(y[0])

print(translated)
print(z)
print(y[0])
print(translatedw)
