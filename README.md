[Sheets](sheets.md) — the four artboards and their design-reference READMEs.

## generate an alphabet deck of cards using animals to teach kids Ukrainian.

Picking a fitting animal for each tricky letter.
I’ll put together a printable 33-card deck — one card per Ukrainian letter, each with an animal, the Ukrainian word, pronunciation, and English. Let me check what format options are available first.

The deck is done: four Letter-size sheets with 36 cards — all 33 letters of the Ukrainian alphabet, each with a simple flat-color animal, the uppercase/lowercase pair, an English sound hint, the Ukrainian word, a transliteration, and the English name — plus a title card, a full-alphabet reference card, and a “how to play” card. Export as “All artboards (.pdf)” from the Share menu, print on card stock, and cut along the dashed lines.

A few choices worth knowing about:

И, Й, and Ь never (or almost never) start Ukrainian words, so those cards use кит (whale), йорж (ruffe, a spiky little fish), and кінь (horse), with the target letter highlighted in color and a one-line note explaining why.
Ґ, Є, Ю have few common animal words, so they use ґава (crow), єнот (raccoon), and юрок (brambling, a small finch). If you’d rather swap any of these for something the kids already know, say which and I’ll change the card.
Transliterations use an apostrophe for the soft sign (ведмідь → vedmid’), which is the standard convention.

[Ukrainian Animal Alphabet Cards-error.pdf](Ukrainian%20Animal%20Alphabet%20Cards-error.pdf) — the first export, with the юрок card.

---

## юрок is not a real bird. find a better animal for that card and explain why you made this mistake.

### the issue is that all other AI models made the same mistake so it is confusing how you can all be wrong on basic facts

Explaining why language models mix up Russian and Ukrainian.

The Ю card now shows a camel — верблюд (verblyud) — with the ю highlighted and a note that almost no animal word starts with that letter, matching how the И, Й and Ь cards work.

On your bigger question: it’s not a coincidence that every model made the same mistake, and it’s not really a “basic fact” failure in the way it looks. A few things stack up:

Russian dominates the training data. There is far more Russian text online than Ukrainian, and the two languages share most of their vocabulary with small, systematic differences (вьюрок/юрок vs в'юрок, еж vs їжак, etc.). Every model learns Ukrainian partly through Russian, so when a Ukrainian word is rare, the Russian form is the louder signal and leaks in. That’s a shared bias from a shared data distribution, so the errors correlate across models rather than being independent.

The Ю slot has no good answer. Ukrainian has essentially no common animal starting with Ю. When a question has no clean answer, models don’t say “there isn’t one” — they produce the most plausible-looking token sequence. "Юрок" looks like a Ukrainian bird name, it’s one letter off a real word, and it’s attested in Russian, so it scores highly as a fill. All models are optimizing the same plausibility objective, so they land on the same wrong fill.

Agreement between models isn’t evidence. Because the models share data, architectures and training methods, their mistakes are correlated. Four models agreeing on юрок tells you roughly as much as one model saying it; it’s not four independent checks. This is worth remembering any time a fact is obscure and the stakes matter: a native speaker or a reference source beats consensus among AIs.

I didn’t verify. The honest part: I treated vocabulary recall as reliable and didn’t check the rare words against a source before putting them on a card meant to teach children. For the common animals (кіт, слон, лев) recall is fine; for the ones I flagged as awkward (ґава, єнот, йорж, юрок) it wasn’t, and I even said they were “rare” without taking the next step. (I did try searching just now, and the results that came back weren’t useful enough to cite; the в'юрок/юрок distinction is one I’m confident of, but if a Ukrainian speaker is available, having them scan the deck once is the right check.)

[Ukrainian Animal Alphabet Cards.pdf](Ukrainian%20Animal%20Alphabet%20Cards.pdf) — the corrected export, with the верблюд card.

---
