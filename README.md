[![make.fun](https://make.fun/badge/news-image-20261118.svg)](https://make.fun/bounty/news-image-20261118)
[![Rank](https://make.fun/badge/news-image-20261118/adeqaila/makefun-news-image-20261118/rank.svg)](https://make.fun/bounty/news-image-20261118)
[![Reward](https://make.fun/badge/news-image-20261118/adeqaila/makefun-news-image-20261118/reward.svg)](https://make.fun/bounty/news-image-20261118)

# The World in One Day — Wednesday, 18 November 2026

Entry for the make.fun bounty **news-image-20261118**: sum up 18 November's
world news in one image.

## The image

A newspaper front page (1024×1024, JPEG under the name `entry.png`), built
from eight AI-generated illustrations with all text drawn as crisp vector
type, so nothing in it can come out garbled. Seven stories, all verified
against reporting dated 18 November 2026:

| Spot | Story |
| --- | --- |
| Lead | **US jets hit Iran's Qeshm site** — US jets strike an IRGC missile site on Qeshm Island after Iran's drones targeted a US radar in Bahrain; a third US carrier joins the Gulf buildup. First reported overnight, 18 Nov in Asian time zones. |
| Asia | **Quad meets in Manila** — first in-person Quad leaders' summit since 2024; Trump heads on to talks in China. |
| Weather | **Cyclone Akvan turns severe** — severe cyclonic storm over the Bay of Bengal; heavy rain from 18 Nov, landfall due 20 Nov, gusts to 145 kmph (IMD). |
| India | **Tanker crew brought ashore** — India condemns the Hormuz tanker attack; 21 of 24 Indian crew evacuated at Khasab. |
| Trade | **Canada and China extend deals** — Xi meets Carney ahead of the APEC summit in Shenzhen. |
| Middle East | **Israel elects a new speaker** — the Knesset chooses Matan Kahana to lead the parliament. |
| Sport | **Portugal top the group** — ten-man Portugal beat Wales to top their Nations League group. |

Deliberately left out (wrong date): the ULA Vulcan failure (15 Nov), the
California AG suit against OpenAI (16 Nov), the Houthi advance toward Aden,
the UK sanctions on Israeli settlement firms (17 Nov), Nvidia's earnings
(17 Nov) and the Russian military plane crash in Siberia (17 Nov).

## The program

`main.ts` (Node 22, standard library only, no network) copies `entry.png`
to the output directory, checking it against the gate first (non-empty, at
most 1 MiB). Both grader runs write identical bytes.

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
```

## Build

`compose.py` renders the front page from the illustrations in `candidates/`
with PIL (DejaVu fonts). Seven variants were built and judged pairwise
against the official criteria; the champion is `variants/v7-final.jpg`
(red masthead, zoomed hero of the destroyed Qeshm missile site, sharper
sublines). See `BUILD-REPORT.md` for the full report.

## License

MIT — see `LICENSE`.
