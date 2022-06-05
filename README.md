# son_topish_oyini.
 Anvar Narzullayev video darslari asosida. Python dasturlash tili.
print("Assalomu Alaykum. son topish o'yiniga xush kelibsiz!!!")
while True:
    import random as r
    sonlar = list(range(1, 11))
    son_a1 = r.choice(sonlar)
    print("Men 1 dan 10 gacha bo'lgan son o'yladim.\nTopa olasizmi?:")
    c = 1
    while True:
        son = int(input(">> "))
        if son > son_a1:
            print("Xato. Men o'ylagan son bundan kichik.")
            c = c+1
        elif son < son_a1:
            print("Xato. Men o'ylagan son bundan katta.")
            c = c+1
        else:
            break
    print(f"Topdingiz. {son_a1} sonini o'ylagan edim. {c} urinishda topdingiz. Tabriklayman!")
    print("1 dan 10 gacha son o'yladim topa olasizmi?")
    input("Son o'ylagan bo'lsangiz istaan tugmani bosing. ")
    son_b = r.choice(sonlar)
    cc = 1
    while True:
        son_b = r.choice(sonlar)
        natija = input(f"{son_b} sonini o'yladingiz: To'g'ri(T), men o'ylagan son bundan kattaroq(+), men o'ylagan son bundan kichikroq(-): ")
        if natija == 'T':
            break
        elif natija == '+':
            sonlar = sonlar[sonlar.index(son_b)+1:sonlar[-1]+1]
            cc = cc+1
        elif natija == '-':
            sonlar = sonlar[0:sonlar.index(son_b)]
            cc = cc+1
    print(f"Soningizni {cc} taxmin bilan topdim.")
    if c == cc:
        print(f"Durrang. Ikkimiz ham {c} taxmin bilan topdik.")
    elif c < cc:
        print("Siz g'olibsiz!")
    elif c > cc:
        print("Men g'olibman!")
    javob = input("Yana o'ynaymizmi? Ha(1), Yoq(0): ")
    if javob == '0':
        break
print("E'tiboringiz ucun raxmat.")
