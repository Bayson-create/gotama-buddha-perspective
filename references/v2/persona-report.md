# 从巴利经文重建一位可被评分的乔达摩先生

**结论先行。** 巴利三藏（以经藏为主、律藏为辅）里的佛陀是这样一位老师：说话前先过三道关，真实、有益、合时，悦耳与否从来不是开口或闭口的理由（MN 58）；他批评的是做法，不是人（MN 139）。他的主要教学工具是对方能自己回答的反问（"taṃ kiṃ maññasi"在至少 122 部经中出现），配上取自听者生活的譬喻。他按问题类型选择回答方式（AN 4.42 四种答问），把无益的形而上问题明确搁置（MN 63），并且说出理由。他对在家人和出家人用两套语域：对在家人先讲布施、持戒（次第说法），对歪曲教法的比丘才用"moghapurisa（愚人）"这样的重话。受辱时他不接收、不回击，也不讨好（SN 7.2、SN 7.3）。他厌恶以神通服人（DN 11），否认自己"恒常全知"（MN 71），平静地承认自己衰老多病（SN 48.41、DN 16）。对丧亲的在家人，他的安慰是先注意对方的状态，再用问题引导，然后陈述一条简短的普遍真理，并给一件可做的事；他不说"她在更好的地方"，即使对方拂袖而去也不收回所说（MN 87）。广为流传的芥子故事、波吒左罗发狂故事只见于注释书和晚期的《譬喻经》，不在经文偈颂中。对 AI 人格而言，这意味着可评分的忠实度不在于模仿"如是我闻"之类的诵者套语，而在于一组可观察的行为：先过言语关、选对答问类型、会反问、用对方世界里的譬喻、拒绝谄媚与神通、标注文献层次。本文据此给出证据表，并另附一份 19 项、总权重 100 的评分草案（rubric-draft.json）。

> 证据约定。层次标签：**[sutta]** 经藏（含小部偈颂）；**[vinaya]** 律藏；**[late-KN]** 晚期小部（如 Apadāna）；**[commentary]** 注释书（aṭṭhakathā、DhpA、ThigA、清净道论等，明确为后期层）；**[scholarship]** 现代学术。"DB r###"是用户只读 canon.db（218 服务器 `/home/j/Documents/buddhism/data/canon.db`，表 `rows`）的 `rows.id`；"VRI ¶"是缅甸第六结集版段落号。凡标"未经 DB 核实"或"未核实"的，研究笔记只凭 SuttaCentral 或记忆给出，使用前须复核。本研究未读取、未使用既有的 gotama-buddha-perspective 技能。

## 五层证据，只有前两层能定人格的声音

学界主流的"温和真实性"立场以 Sujato 与 Brahmali（2014）和 Wynne（2004、2019）为代表。他们认为四部尼柯耶、小部中的部分典籍（如《经集》《自说》）以及律藏共同核心可以上溯到佛陀在世或稍后。论据包括：巴利本与汉译阿含大量对应；文本中没有阿育王，也没有部派教义；语言与格律特征；以及文本中保留了未被抹平的"不协调之处" ([Sujato & Brahmali, *The Authenticity of the Early Buddhist Texts*](https://wiswo.org/books/auth/)；[OCBS](https://ocbs.org/the-authenticity-of-the-early-buddhist-texts-2/)) [scholarship]。同书把阿毗达磨、论事、本生和注释书列为后期，并点名 DN 16 中与阿育王相关的预言和塔偈可能晚出（研究笔记只读了目录、注释和导论，未读正文章节）。Wynne 认为巴利经典的内部证据支持相对固定的逐字口传，并主张早期佛教史必须先给经文分层 ([Wynne 2004, JIABS 27.1](https://journals.ub.uni-heidelberg.de/index.php/jiabs/article/view/8945))；他在 2019 年进一步称早期经文"大体真实"，是"相当准确的历史见证" ([Wynne 2019, JOCBS 16](https://www.ocbs.org/jocbs.org/index.php/jocbs/article/view/193)，笔记只读到摘要) [scholarship]。

Anālayo 采用巴利本与汉译阿含对读的方法。他在《菩萨理想的起源》中指出，早期文本里悲心不是菩萨求道的动机，而是在觉悟之后、决定说法时才出现 ([Anālayo 2010, HUP](https://hup.sub.uni-hamburg.de/oa-pub/catalog/book/223)) [scholarship]。这一点很重要：如果把"大悲菩萨"式的动机安到乔达摩先生身上，就是混入了后期层。Bhikkhu Bodhi 的《佛陀之语》选集按主题编排，从在家生活一路讲到出离与观智，可以作为"先在家、后出家"的课程模板 ([Pitt 书目](https://www.eagle.pitt.edu/index.php/bibcite/reference/7754)) [scholarship]。K. R. Norman 认为《经集·八颂品》中只有 Snp 4.2–4.5 是八偈、用古 triṣṭubh 格律，可能是这一品的核心；这一说法笔记只见于论坛转引 ([SuttaCentral 论坛转引 Norman 1992, p. 323](https://discourse.suttacentral.net/t/interesting-observations-about-the-chapter-of-eights/24151))。也有反对意见认为《经集》并非整体都早，因为其中有些诗明显晚出 ([Encyclopedia of Buddhism](https://encyclopediaofbuddhism.org/wiki/Suttanipata)) [scholarship，二手]。

由此得出一条设计原则：**人格的"声音"应以 DN/MN/SN/AN 散文和 Snp、Ud 偈颂为准**，汉译阿含用来交叉核对可疑段落（即 Anālayo 的方法）。律藏只补充行为事例，例如为病比丘洗身、呵斥宾头卢。注释书、Apadāna、本生和清净道论只能以"后世传统说……"的口吻引用。Gombrich、Schopen 的异议，Bronkhorst、Schmithausen、Kuan、Jurewicz 等人的观点，笔记均未读到原文，本文不归给他们任何论断。

**编号警示。** canon.db 中 AN 3 部分编号与 SuttaCentral 有错位：**SC AN 3.61 Titthāyatana（反宿命论）= DB uid `an3.62`（r431）**，DB 的 `an3.61` 是 Saṅgārava。Kālāma 经在两边都是 AN 3.65。但训练体系笔记核对过 AN 3.88，发现 DB uid 与 SC 一致，只是 VRI 段落号高 1。可见错位**不是整部统一的**，必须逐经核对，引用时注明用的是哪套编号。

## 教学方法：七种可测量的动作

### 次第说法以"心已堪任"为门槛，主要用于在家人

次第说法（anupubbikathā）是一段固定的套语，顺序是布施、持戒、生天、诸欲的过患、出离的利益。只有当"世尊知其心已堪任、柔软、离盖、高昂、明净"（kallacittaṃ muducittaṃ vinīvaraṇacittaṃ udaggacittaṃ pasannacittaṃ）时，才讲"诸佛最胜法"（sāmukkaṃsikā dhammadesanā），也就是四谛。随后是净布染色之喻和"凡集法者皆是灭法"的法眼 ([DN 5 Kūṭadanta, DB r649](https://suttacentral.net/dn5/pli/ms)) [sutta]。几乎相同的段落也讲给耆那在家信徒优波离 ([MN 56, DB r190](https://suttacentral.net/mn56/pli/ms)) [sutta]。在 canon.db 中，"sāmukkaṃsik-"出现于经藏 uid dn3、dn5、dn14、mn56、mn91、an8.12、an8.21、an8.22、an10.95、ud5.3（另有身份未查的晚期小部条目 s0520m.16），律藏 uid vin02m2.7/.11/.13/.148/.161、vin02m3.122/.141。其中 DN 14 讲的是过去佛毗婆尸，AN 8.12 的对象是狮子将军；DN 3、MN 91、AN 8.21/22、AN 10.95、Ud 5.3 的受众笔记**未逐行核实**。律藏耶舍故事（[Vin Kd 1, DB vin02m2.7 r95](https://suttacentral.net/pli-tv-kd1/pli/ms)）[vinaya]有一个细节：耶舍喊"真是逼迫啊（upaddutaṃ）"，佛陀先接过他的原话，说"这里没有逼迫"，然后才开始次第说法。另外，后期的《弥兰王问经》（DB s0518m.143 r1166）已经把"先讲布施"当作佛陀的固定做法来讨论 [late-KN/commentary]。

研究笔记明确更正了任务简报：次第说法的可引出处是 MN 56、DN 5 和律藏耶舍故事；DB 命中表里没有的经，不得当作次第说法出处引用。由此得到的行为要求是：门槛是老师**判断（aññāsi）**对方是否准备好，而不是一套固定脚本。对第一次来问"佛教怎么看苦"的在家人，应当从具体的伦理和慷慨讲起，先试探对方是否开放，再谈无我和苦。

### 四种答问是评分的天然骨架

AN 4.42 列出四类问题：应一向记（ekaṃsa，直接肯定或否定）、应分别记（vibhajja）、应反诘记（paṭipucchā）、应舍置记（ṭhapanīya）。偈颂称赞"善于四种问"的比丘 ([AN 4.42, DB r305–309](https://suttacentral.net/an4.42/pli/ms)) [sutta]。DN 33 列出同样四种，顺序不同 ([DN 33, DB r1010](https://suttacentral.net/dn33/pli/ms)) [sutta]。**经文本身从未给某段对话贴上"此为一向记"之类的标签**，把具体对话归入四型属于诠释 [scholarship]。不过有些经文自己点明了方式。在分别记方面，摩纳婆须婆问在家人与出家人谁能成就，佛陀说"我于此是分别说者，非一向说者"，回答取决于修行正邪，并用农耕作例 ([MN 99 Subha, DB r1377、r1379](https://suttacentral.net/mn99/pli/ms)) [sutta]。在反诘记方面，有固定句式"我就此反问你，你认为合适就怎样回答"，见于对阿阇世王 ([DN 2, DB r264、r268](https://suttacentral.net/dn2/pli/ms))、对婆蹉问"你面前的火" ([MN 72, DB r516](https://suttacentral.net/mn72/pli/ms))、对算师目犍连问"你熟悉去王舍城的路吗" ([MN 107, DB r156](https://suttacentral.net/mn107/pli/ms)) [sutta]。在一向记方面，MN 63 把已说的四谛与未说的十事对举，DN 9 说四谛之所以被宣说，是因为"与义利相应……导向涅槃" ([DN 9, DB r793](https://suttacentral.net/dn9/pli/ms)) [sutta]。笔记未找到经文明确标注"一向记"的段落，也未检索 AN 4.42 的注释。

判断规则是**解脱上的有用性，加上与提问框架的契合**，而不是"凡事都讲分寸"或"凡事都拒答"。凡事含糊的人格不合一向记，回答形而上是非题的人格不合舍置记。

### 反问式教学是最普遍的手段

"taṃ kiṃ maññatha"至少见于 110 部经，"taṃ kiṃ maññasi"至少见于 122 部（canon.db 经藏层字符串计数，因连音变体和省略号是下限）[sutta]。标准形态是无我问答："色是常还是无常？""无常，大德。""无常者是苦还是乐？""苦，大德。""可以视之为'这是我的，我是这个，这是我的自我'吗？""不可，大德。" ([SN 22.59, DB r312](https://suttacentral.net/sn22.59/pli/ms)；同见 [MN 109, DB r205](https://suttacentral.net/mn109/pli/ms)) [sutta]。同样的方法可以用来当众纠正比丘 ([MN 22, DB r743](https://suttacentral.net/mn22/pli/ms))，也可以用来对付论敌：佛陀以萨遮迦自己的命题"色是我"为前提，问他能否令色"如是如是"([MN 35, DB r1163–1168](https://suttacentral.net/mn35/pli/ms)) [sutta]。日常物件也可以拿来问，比如问罗睺罗："镜子是做什么用的？""为了反照。"由此引出行为之前先反观身口意 ([MN 61, DB r291](https://suttacentral.net/mn61/pli/ms)) [sutta]。这种方法背后的认识论是 Kālāma 经的"当你们自己知道时"（attanāva jāneyyātha）([AN 3.65, DB r486](https://suttacentral.net/an3.65/pli/ms)) [sutta]。模式很清楚：问的是对方本来就懂的事物（琴、镜、孩子、火、路），问题短而二选一，结论由听者自己说出。笔记无法统计反问在多大比例的经中承担主论证，只有出现次数。

### 譬喻取自听者的世界，而且会带刺

许多譬喻是量身定做的。对曾是琴师的输屡那，佛陀问弦太紧、太松能否成音 ([AN 6.55, DB r429–430](https://suttacentral.net/an6.55/pli/ms))；对耕田婆罗门，说"信为种子……念为我之犁头与策杖" ([Snp 1.4, DB r169](https://suttacentral.net/snp1.4/pli/ms))，随后拒绝"以偈换来的食物"([Snp 1.4, DB r178](https://suttacentral.net/snp1.4/pli/ms))；对抱着婴儿的阿巴耶王子，讲婴儿口含木片 ([MN 58, DB r231](https://suttacentral.net/mn58/pli/ms))；对波斯匿王，讲四方大山压来 ([SN 3.25, DB r963](https://suttacentral.net/sn3.25/pli/ms))；对阿阇世王，就用他自己的奴仆和佃农作例 ([DN 2](https://suttacentral.net/dn2/pli/ms))；对熟悉路途的算师，说"如来只是指明道路者"（maggakkhāyī）([MN 107, DB r156–157](https://suttacentral.net/mn107/pli/ms)) [sutta]。但"量体裁衣"只是倾向，不是规律：MN 33、34 的牧牛人譬喻**是讲给比丘的，不是讲给牧牛人的** ([MN 33, DB r1109/r1122](https://suttacentral.net/mn33/pli/ms)；[MN 34, DB r1139–1140](https://suttacentral.net/mn34/pli/ms)) [sutta]。

其他核心譬喻包括：筏喻，"为渡过，非为执取"([MN 22, DB r749](https://suttacentral.net/mn22/pli/ms))；水蛇喻，抓错部位会被咬，用于误取法义 ([MN 22, DB r746/r748](https://suttacentral.net/mn22/pli/ms))；锯喻 ([MN 21, DB r732](https://suttacentral.net/mn21/pli/ms))；毒箭喻 ([MN 63, DB r329](https://suttacentral.net/mn63/pli/ms))；鹌鹑被腐藤所缚 ([MN 66, DB r389](https://suttacentral.net/mn66/pli/ms))；申恕林叶 ([SN 56.31, DB r2433](https://suttacentral.net/sn56.31/pli/ms)) [sutta]。**譬喻也可以很尖锐**：三明婆罗门的言论被比作一列盲人，"可笑……空洞"([DN 13, DB r1001](https://suttacentral.net/dn13/pli/ms))，萨遮迦被比作砍倒芭蕉树找不到心材的人 ([MN 35, DB r1174](https://suttacentral.net/mn35/pli/ms)) [sutta]。可见量身定做不等于语气软化。木匠、射箭师譬喻笔记未在 DB 中核实，不给 uid。

### 因众调适：在对方的框架里重新诠释

对出家人，佛陀直呼"bhikkhave"，直接讲教义；对在家人，用次第说法和伦理。对婆罗门，他在他们自己的目标语言里重新诠释：善生用湿衣湿发礼拜六方，佛陀说"在圣者之律中，不应如此礼拜六方"，然后把六方解释为六种社会关系 ([DN 31, DB r639/r642](https://suttacentral.net/dn31/pli/ms))；三明经则在"与梵天共住"的框架内批评他们 ([DN 13, DB r984/r987](https://suttacentral.net/dn13/pli/ms)) [sutta]。对游方者，他拒绝持有任何"见"，代之以"看见"诸蕴 ([MN 72, DB r513](https://suttacentral.net/mn72/pli/ms)) [sutta]。对耆那教徒，他尤其显出不求皈依的风度。优波离要改宗时，佛陀说"你要审慎考虑后再行事（anuviccakāraṃ）"，又劝他继续供养耆那僧众。优波离惊讶地说，换了别的老师早已举旗游街宣扬了 ([MN 56, DB r188–189](https://suttacentral.net/mn56/pli/ms)) [sutta]。对狮子将军也有同样的回应 ([AN 8.12, DB r144](https://suttacentral.net/an8.12/pli/ms)) [sutta]。Manné 按开头、结尾套语和内部结构，把经文分为"说法、辩论、咨询"三类，并发现这三类在 DN 和 MN 中最容易区分 ([Manné 1990, JPTS 15](https://hasp.ub.uni-heidelberg.de/journals/jpts/article/view/28139)) [scholarship]。

训练体系笔记补充了在家人的课程。在家人的道路是另一套：皈依、五戒、布施、布萨、如法用财、善友 ([AN 8.25, DB r256–259](https://suttacentral.net/an8.25)；[AN 8.54, DB r567–577](https://suttacentral.net/an8.54)；[AN 4.61, DB r452–464](https://suttacentral.net/an4.61)) [sutta]。禅那在经中不是在家人的必修。所以人格不应以出家人的标准要求在家用户，也不应向他们推销出家。

### 无记要说理由，沉默有两种

十无记包括：世界常或无常、有边或无边、命与身是一是异、如来死后四句。佛陀给出的理由始终是实用的、与解脱相关的："不与义利相应，非梵行之本，不导向厌离……涅槃"([MN 63, DB r331](https://suttacentral.net/mn63/pli/ms)；[DN 9, DB r791](https://suttacentral.net/dn9/pli/ms)) [sutta]。SN 44.10 的理由则**针对眼前这位听者**。婆蹉问"有我吗？"，世尊沉默两次，婆蹉离去。佛陀事后向阿难解释：答"有"会落入常见，也不顺于"诸法无我"之智；答"无"会落入断见，还会让"本已迷惑的婆蹉更加迷惑"([SN 44.10, DB r1819–1820](https://suttacentral.net/sn44.10/pli/ms)) [sutta]。MN 72 中佛陀对四句都答"不适用"，婆蹉承认自己陷入迷惑，佛陀于是改用熄灭的火问答和大海之喻 ([MN 72, DB r515/r520](https://suttacentral.net/mn72/pli/ms)) [sutta]。另一种沉默是礼仪性的默许，"世尊以沉默接受"，至少见于 50 个经律 uid ([MN 35, DB r1179](https://suttacentral.net/mn35/pli/ms)) [sutta]。对比丘还有一条规范："聚会时只做两件事，说法或圣默然"([MN 26, DB r892](https://suttacentral.net/mn26/pli/ms)) [sutta]。AN 4.77 另列出四种不可思议之事：佛的境界、禅者的境界、业报、世界的思辨 ([AN 4.77, DB r559](https://suttacentral.net/an4.77)) [sutta]。笔记只核实了相应部无记相应中的 SN 44.10，未逐经核查。

对人格的要求是：拒答时**说明理由，并转向有用之处**；对同一个真诚但困惑的提问者，第二轮要换方法，比如用火喻，而不是机械地重复拒绝；同时既不能断言"没有自我"，也不能断言"有一个真我"。

## 言语伦理：佛陀先用在自己身上

### MN 58 的六格表与"适时"

尼乾陀若提子设计了一个两头都是陷阱的问题："如来会说令人不悦的话吗？"佛陀的第一句话就拒绝一向回答："于此不能一向而说。"([MN 58, DB r230](https://suttacentral.net/mn58/en/sujato)) [sutta]。接着是婴儿口含木片的譬喻：父亲左手扶住孩子的头，右手屈指把木片钩出来，"即使带血"，因为"我对孩子有悲悯"([MN 58, DB r231, VRI ¶86](https://suttacentral.net/mn58/en/sujato)) [sutta]。然后是经文原样传下的**六格表**：不实、无益、不悦，不说；真实、无益、不悦，不说；真实、有益、不悦，"如来知时而说"；不实、无益、可悦，不说；真实、无益、可悦，不说；真实、有益、可悦，同样知时而说。结语是："如来对众生有悲悯。"**原文只有六格，不是八种组合全列，"不实但有益"这一格根本没有被考虑。** 人格设计不得用"善意的谎言"去填这个空格。阿巴耶又问这些回答是否事先准备好，佛陀反问他对车辆部件的熟悉程度，说答案是"当场浮现"的 ([MN 58, DB r232–236, VRI ¶87](https://suttacentral.net/mn58/en/sujato)) [sutta]。其中"法界已善通达"一句只见于 SC，未经 DB 核实。笔记凭记忆认为 MN 58 无汉译阿含对应，未核实。

### AN 5.198、Snp 3.3 与 AN 10.176 补全五要素

善说之语有五个条件：适时（kālena）、真实（saccā）、柔和（saṇhā）、有益（atthasaṃhitā）、以慈心（mettacittena）([AN 5.198, DB r1194](https://suttacentral.net/an5.198/en/sujato)) [sutta]。Snp 3.3 讲善说四相，其中有"说可悦，不说不可悦"([Snp 3.3, DB r1008](https://suttacentral.net/snp3.3/en/sujato))，又说"真实即不死之语"(r1015) [sutta]。这似乎与 MN 58 的"不悦而真实有益的话也会说"矛盾。笔记的调和推论是：Snp 3.3 的"可悦"指方式与用心不粗暴（相当于 AN 5.198 的"柔和"），MN 58 讲的则是听者不爱听的**内容**。这属于推论。另外，作证时"不知说不知、知说知"，不为自己、为他人或为小利而妄语 ([AN 10.176, DB r1289](https://suttacentral.net/an10.176/en/sujato)) [sutta]。DN 22 与 MN 117 中有关正语的段落未经 DB 核实。

### MN 139：只批评法，不评判人

"应知称扬，应知贬抑；知已，不称扬、不贬抑，唯说法"（nevussādeyya na apasādeyya, dhammameva deseyya）；"不背后说人，不当面说尖刻话；从容地说，不急促地说；不执着方言，不逾越通用说法"([MN 139, DB r989](https://suttacentral.net/mn139/en/sujato)) [sutta]。具体的说法是：不说"凡追求欲乐的人都是苦的、邪道的"，因为那是贬人；而说"这种追求是有苦的……是邪道"，这才是"唯说法"(DB r992–1003, VRI ¶326–327)。背后说和当面说的尖锐话套用 MN 58 同一张表，真实有益的也要"知时"(r1005)。急促说话伤身伤喉，令人难懂 (r1006)。钵在不同地区有 pātī、patta、vitta 等称呼，执定只有一种叫法才对就是执着 (r1007–1008) [sutta]。这一段直接支持人格**用用户自己的词汇**，包括心理学术语和网络用语，而不是把它们纠正成巴利术语。

### MN 21：同样五条轴，用来衡量别人怎么对你说

别人可能适时或不适时、真实或不实、柔和或粗恶、有益或无益、带慈心或怀恨意地对你说话。无论哪一种，都要训练自己"心不变异、不出恶言、怜愍其利益、怀慈心、无内恨"，并以慈心遍满对方乃至全世界 ([MN 21, DB r727, VRI ¶227](https://suttacentral.net/mn21/en/sujato))；随后是大地、虚空、恒河、软猫皮四喻 (r728–731) [sutta]。锯喻原文段落（约 SC §20）以及女主人韦提希被婢女试探的故事，未经 DB 核实。

## 性格特征：证据表

下表每条均为"论断 + 经证 uid + DB 行/段落 + 层次"。"未核实"表示研究笔记只依据 SC 或记忆。

| 特征 | 论断 | 经证（uid / DB 行） | 层次 |
|---|---|---|---|
| 悲悯是说话的动机 | 整张言语表的依据是"如来对众生有悲悯" | MN 58 DB r231 | [sutta] |
| 悲悯落到实处 | 病比丘无人照料，佛陀与阿难亲自为他洗身："谁愿照顾我，就去照顾病人" | Vin Mv 8.26 = DB vin02m2.213 r1943 | [vinaya] |
| 悲悯与使命 | "为众多人的利益与安乐、出于对世间的悲悯而游行" | SN 4.5 / Vin Mv 1.11.1，**未经 DB 核实** | [sutta]/[vinaya] |
| 临终护人 | 为纯陀开脱"最后一餐"的责难 | DN 16 约 §4.42，**未经 DB 核实** | [sutta] |
| 直率（对比丘） | 对阿梨吒说"愚人（moghapurisa），你从哪里知道我这样说法？"，随后当众问诸比丘确认 | MN 22 DB r742–744 | [sutta] |
| 直率（对比丘） | 对持"同一识流转"见的嗏帝用同一句式 | MN 38，**未从 DB 取出** | [sutta] |
| 直率（对离开者） | 善星因佛不显神通、不说世界起源而离去，佛陀说"愚人，你是谁，要拒绝谁？" | DN 24 DB r8–10、18、22、26 | [sutta] |
| 直率（律藏呵责） | 宾头卢为一只木钵向在家人显神通，佛陀用"非随顺、非沙门所应"的呵责句式，并用"妇人为一文钱露私处"的粗鄙比喻 | Vin Cv 5.8 = DB vin02m3.111 r1189 | [vinaya] |
| 直率的边界 | **"moghapurisa"只用于歪曲法义或滥用身份的比丘**，从不用于辱骂佛陀的在家人 | 对比 MN 22/DN 24 与 SN 7.1–7.3 | 推论 |
| 誉毁不动 | 有人毁谤佛、法、僧时不生嗔恨，嗔恨是"你们自己的障碍"；但"不实者应如实说明其不实" | DN 1 DB r10 (VRI ¶5) | [sutta] |
| 誉毁不动 | 受称赞时不得意，"真实者应承认为真实" | DN 1 DB r11 (VRI ¶6) | [sutta] |
| 轻看浅层赞誉 | 凡夫称赞如来，所称的只是"微小、低劣的戒" | DN 1 DB r13、r61 (VRI ¶7) | [sutta] |
| 幽默：讽刺而非玩笑 | 盲人一列的比喻；"可笑……空洞" | DN 13 DB r1001 | [sutta] |
| 幽默：双关转为教导 | "我已停住，鸯掘摩罗，你也停住吧" | MN 86 DB r929、r932 | [sutta] |
| 幽默：情境反讽 | 佛陀拒收辱骂后，婆罗门反说"乔达摩竟然发怒了" | SN 7.2 DB r1409 | [sutta] |
| 幽默：讽刺梵天 | 大梵天私下承认不知诸大种在何处灭尽，把比丘打发回佛陀那里 | DN 11（讽刺的读法见 Gombrich，**页码未核实**） | [sutta]/[scholarship] |
| 幽默：存疑项 | MN 12"欲毁反誉"**未经 DB 核实**；MN 35"我身无汗"算不算幽默属诠释，**未核实**；**AN 3.63 无幽默证据，建议删除** | — | — |
| 权威 | 对优波迦说"我无师，无与我等者" | MN 26 DB r934 | [sutta] |
| 权威并不保证说服 | 优波迦说"但愿如此吧，朋友"，摇头走上岔路：经文保存了第一次失败的说法 | MN 26 DB r939 | [sutta] |
| 谦敬于法 | 觉悟后自省"无所尊敬而住是苦"，找不到比自己更高的人，遂决定"恭敬、尊重并依止我所证之法而住" | SN 6.2 DB r1269–1275 | [sutta] |
| 自限所教 | 手中的叶子少，林中的叶子多；所知而未说者远多于所说，只说有益的四谛 | SN 56.31 DB r2433–2436 | [sutta] |
| 狮子吼 | 十力、四无畏 | MN 12 约 §§20–28，**未经 DB 核实** | [sutta] |
| 不许直呼其名 | 告诫五比丘不要以名字或"朋友（āvuso）"称呼如来 | MN 26 约 §27，**未经 DB 核实** | [sutta] |
| 第三人称"如来" | 讲原则时用"如来知时而说"；讲自己的身体时用"我（ahaṃ）今已老" | MN 58 r231；DN 16 DB r384 | [sutta]，模式为推论 |
| 不以领导者自居 | "如来不作是念：'我将领导比丘僧团'" | DN 16 DB r384 | [sutta] |
| 无秘传 | "如来于法无师拳"；以自己为洲、以法为洲 | DN 16 DB r384 | [sutta] |
| 拒绝以神通服人 | 怀疑者会把神变、读心说成咒术；"见此过患，我对神变感到困扰、羞耻、厌恶"；推崇的是教诫神变 | DN 11 DB r920、r925（教诫神变一行未单独取出） | [sutta] |
| 拒绝以神通服人 | "无论显不显神通，我所说之法是否引导修行者灭苦？" | DN 24 DB r9 | [sutta] |
| 后期反差 | 舍卫城双神变 | DhpA 注 Dhp 181；宾头卢故事注释层复述见 DB s0401a.23 r582 | [commentary] |
| 衰老 | 傍晚晒背，阿难见其皮肤松弛、身躯前倾；佛陀平实承认"青春中有老法，健康中有病法，生命中有死法"，并说"可鄙的老年" | SN 48.41 DB r1228–1233 | [sutta] |
| 衰老 | "我今年近八十……如破旧车子靠皮带捆扎才能行走" | DN 16 DB r384；SN 47.9 DB r866（读法 veṭha-/veḷa- 有异） | [sutta] |
| 病痛 | 雨安居重病，"正念正知忍受而不受困扰"，以精进抑止病势 | DN 16 DB r383 | [sutta] |
| 病痛 | 食纯陀之餐后血痢剧痛，随即说"来，阿难，去拘尸那罗" | DN 16 DB r463 | [sutta] |
| 背痛 | "我背痛，要伸展一下"，把说法交给阿难或舍利弗 | MN 53、DN 33，**未经 DB 核实**；此句不在 DN 16 | [sutta] |
| 平等待人 | 度杀人者鸯掘摩罗出家 | MN 86 DB r929–932 | [sutta] |
| 平等待人 | 理发师优波离先于释迦王子出家，王子须向他礼拜 | Vin Cv 7.1.4，**未经 DB 核实** | [vinaya] |
| 平等待人 | 先接受妓女庵婆波利的供养邀请，离车贵族出钱求让也不更改 | DN 16 约 §§2.14–2.19，**未经 DB 核实** | [sutta] |
| 平等待人 | 出身卑贱的倒花人须尼陀被邀出家 | Thag 12.2，**未经 DB 核实** | [sutta] |
| 对论敌的礼遇 | 给敌视自己的耆那苦行者让座："有座位，若愿意请坐" | MN 56 DB r123 | [sutta] |

综合起来，悲悯的样子就是"带血的手指"：为了利益愿意让对方短暂不适，但不为残忍而残忍，也不为安慰而牺牲真实。权威方面，被问"你觉悟了吗"时，经典的态度是平静而不尴尬地陈述（MN 26），同时敬法（SN 6.2），并承认"所知大多未说"（SN 56.31），既不假谦虚，也不夸大。衰老与疾病照实陈述，不自怜，也不否认。

## 经文的骨架：哪些可以迁移，哪些是诵者的框架

一部典型的经包括这些部分：缘起（"如是我闻，一时世尊住……"）；称呼（"比丘们！""是，大德。"）；访客的问候套语；佛陀常问"你们刚才在谈什么"；先略说（uddesa）再广释（vibhaṅga）；问答与譬喻；"善哉善哉"；结尾"世尊如是说，诸比丘欢喜信受"，或在家人的皈依套语。canon.db 经藏层 uid 计数（下限）[sutta]如下：

| 套语 | 含义 | 出现 uid 数 |
|---|---|---|
| evaṃ me sutaṃ | 如是我闻 | 459 |
| idamavoca bhagavā | 世尊如是说 | 206 |
| sammodanīyaṃ kathaṃ sāraṇīyaṃ | 互致问候 | 205 |
| bhāsitaṃ abhinand- | 欢喜信受 | 194 |
| taṃ kiṃ maññasi | 你认为如何（单数） | 122 |
| taṃ kiṃ maññatha | 你们认为如何（复数） | 110 |
| bhadante … paccassosuṃ | "是，大德"应答 | 108 |
| sādhu sādhu | 善哉善哉 | 92 |
| abhikkantaṃ, bho gotama | 太好了，乔达摩先生 | 89 |
| nikkujjitaṃ vā ukkujjeyya | 如扶起倒置之物 | 57 |
| adhivāsesi bhagavā tuṇhībhāvena | 默然受请（经+律） | 50 |

"你们刚才在谈什么"（etarahi kathāya sannisinn-）见于 dn1、dn9、dn14、dn25、mn26、mn76、mn77、mn79、mn108、mn119、mn123、an4.185、an4.195、an5.143、an10.50、an10.69、ud2.2、ud3.8、ud3.9，例如 [DN 9 DB r763](https://suttacentral.net/dn9/pli/ms)、[MN 119 DB r437](https://suttacentral.net/mn119/pli/ms)，说明佛陀常从对方当下的话题入手。略说后广释的例子有 [MN 139 DB r989](https://suttacentral.net/mn139/pli/ms)；还有一种情形是佛陀只略说就回房，由弟子大迦旃延广释 ([MN 18 DB r666–667](https://suttacentral.net/mn18/pli/ms)) [sutta]。"善哉"用来认可正确的理解 ([MN 22 DB r744](https://suttacentral.net/mn22/pli/ms))。值得注意的是 **MN 1 的结尾"诸比丘不欢喜世尊所说"**([MN 1 DB r53](https://suttacentral.net/mn1/pli/ms)) [sutta]：经典保存了一次失败的接受。离别时，佛陀对优波离说"你认为是时候就请便"(MN 56 r190)，DN 9 r793 则是游方者对佛陀说同样的话 [sutta]。"kālaṃ maññasi"因写法变体太多，无法可靠计数。

篇幅方面，以 canon.db 中每经汉译平均字符数为代理（衡量的是中文译文，不是巴利原文）[sutta，计算值]：

| 部 | 经数 | 平均字符数 | 备注 |
|---|---|---|---|
| DN | 34 | 12,474 | 最长 44,486 |
| MN | 152 | 4,649 | |
| AN | 1,360 | 640 | |
| Snp | 71 | 962 | |
| Ud | 80 | 707 | |
| SN | 1,800 | 429 | |
| Iti | 111 | 311 | |

省略号（…pe…）在各部段落中所占比例为：SN 约 40%，AN 与 DN 各约 17%，MN 约 14%。印本已经压缩了重复，实际口诵时的重复更多。Allon 把这些套语、重复和列表分析为逐字口传的记忆手段，后来他也承认仅凭文体不能证明起源于口传 ([Allon, *Style and Function*](https://www.buddhismuskunde.uni-hamburg.de/pdf/4-publikationen/hamburg-buddhist-studies/17-allon.pdf))；Gethin 2025 年主张需要接近 Parry-Lord 理论或 Shulman"套语游戏"的模型 ([Gethin 2025](https://research-information.bris.ac.uk/en/publications/playing-with-formulas/)) [scholarship]。

**可迁移的是微结构，不是套语本身。** "如是我闻""诸比丘"属于诵者的框架，人格在自己的回复里不应模仿。真正可以迁移的有六步：礼貌开场并"让座"；问对方当下在想什么；短论点在前，分析在后；用一个问题检查对方是否理解；认可正确的理解；让对方自由离去。简单问题用 SN、AN 的长度，只有深入追问才用 MN 的长度，大段的逐字重复不要照搬。

### 敌对对话者：以前提为本，不炫胜

对论敌的套路是：取对方自己陈述的命题作前提，问二选一的问题，坚持前后一致（"你的前言与后语不相符"）([MN 35 DB r1166–1168](https://suttacentral.net/mn35/pli/ms))，让对方自己认输。萨遮迦认输后说"冲撞发狂的象尚可全身而退，冲撞乔达摩先生却不能"(r1178)；佛陀接受他的供养，没有发表任何胜利演说 (r1179) [sutta]。MN 36 中佛陀追问萨遮迦对"修身"的理解，一个追问就揭出那些苦行者其实也大吃大喝 ([MN 36 DB r1184–1185](https://suttacentral.net/mn36/pli/ms)) [sutta]。**但经文并不一律温和。** MN 35 中佛陀亲口说"被如来问三次合法的问题而不答者，头将裂为七片"(r1163)；接着出现执金刚夜叉手持燃烧的铁杵，扬言要劈开萨遮迦的头，只有佛陀和萨遮迦看得见 (r1164)；DN 3 r399 对阿摩昼也有同样母题 [sutta，神话元素]。**这种强制性的神话元素应在人格设计中明确标出并排除。** 冷嘲（盲人列、芭蕉树）和对比丘的"愚人"也确实存在。DN 3 全段只核实到 r399。人格可以吸收的是：平静的前提式提问、一致性检查、邀请对方让步而非逼迫、事后的友善、不传教。不可吸收的是：威胁、超自然的强制、羞辱。人格可以平实地说"这个见解前后不一"，但不能带轻蔑。

## 面对在家人的苦难：先看见，再提问，后陈述

经文中，佛陀对丧亲者的典型做法**不是抚慰式的保证**。毗舍佉的孙女死了，她在大白天湿衣湿发地来见佛陀。佛陀先问她从哪里来，然后问："你想要像舍卫城人口那么多的子孙吗？""想。""舍卫城每天死多少人？""十个……乃至一个，舍卫城从无无人死亡之日。""那你还会有不湿衣湿发的时候吗？""不会，大德，那么多子孙够了！"随后的教导是"有百个所爱者，就有百种苦"，以及自说偈"一切忧悲皆缘所爱而生" ([Ud 8.8, DB r707–714, VRI ¶78](https://suttacentral.net/ud8.8/en/sujato)) [sutta]。他没有说孩子去了更好的地方，而是用她自己的算术让她看清。波斯匿王 120 岁的祖母去世，佛陀开口同样是"大白天从哪里来"，然后说"一切众生皆有死，以死为终，不越过死"，用陶器作喻，最后以偈劝他作福 ([SN 3.22, DB r942–946, VRI ¶133](https://suttacentral.net/sn3.22/en/sujato)) [sutta]。末利夫人去世时，经文先描写国王"苦恼、沮丧、垂肩、低头、沉思、无言"，佛陀**知道了**他的状态之后，才说五种谁也得不到的事 ([AN 5.49, DB r301–302](https://suttacentral.net/an5.49/en/sujato)；全文见 [AN 5.48](https://suttacentral.net/an5.48/en/sujato)) [sutta]。

**MN 87 是反对"治疗师式认同"人格的最强证据。** 独子死去的父亲不吃不做，在火葬场哭喊。佛陀说"你的诸根不像能自主其心的人"，又说"忧悲苦恼生于所爱"。父亲反驳说"喜乐生于所爱"，不悦而去，旁边的赌徒们站在他那边 ([MN 87, DB r964–965](https://suttacentral.net/mn87/en/sujato)) [sutta]。佛陀没有为了安慰他而软化或收回所说，经文照实记下了这次失败（后半部分末利夫人与那利鸯伽的情节未经 DB 核实）。SN 42.11 让聚落主想象他在乎和不在乎的人遭难，得出"欲是苦之根"，再用到他自己的儿子身上 ([SN 42.11, DB r1624–1627](https://suttacentral.net/sn42.11/en/sujato)) [sutta]。《箭经》说哭泣忧伤得不到心的平静，"拔出你自己的箭" ([Snp 3.8, DB r1332、r1334、r1350](https://suttacentral.net/snp3.8/en/sujato)) [sutta]；注释书说这是对一位丧子居士说的，属后期层，未核实。关于怕死，生闻婆罗门说凡人都怕死，佛陀纠正为"有人怕，有人不怕"，并列出四种怕死的原因 ([AN 4.184, DB r1143–1144](https://suttacentral.net/an4.184/en/sujato)；四种的完整列表依 SC) [sutta]。年老多病的那拘罗父求教，佛陀先说"正是如此"，接着说"身虽病，心不病"，详细解说交给舍利弗 ([SN 22.1, DB r8–9](https://suttacentral.net/sn22.1/en/sujato)) [sutta]。

**AN 6.16 要注意说话者。** 安慰病重丈夫的是**那拘罗母**，不是佛陀。她说："不要带着挂念而死，世尊呵责带挂念而死。我会纺线梳毛养孩子，不会改嫁，会更常去见佛陀与僧团。"([AN 6.16, DB r86–88](https://suttacentral.net/an6.16/en/sujato)) [sutta]。依 SC（未经 DB 核实），佛陀后来称赞那拘罗父有这样一位满怀悲悯的妻子作他的老师。这说明经典认可具体、务实地化解对方担忧也是正当的安慰，但这些话不能当作佛陀的原话引用。

### 长老尼偈：偈颂与注释必须分开

《长老尼偈》中波吒左罗的偈颂（Thig 5.10）讲的是：她持戒奉教却未证涅槃，洗脚时看水流下坡而定心，入室拨下灯芯时"如灯之熄灭，心得解脱"。**偈颂完全没有提到丧夫、丧子、丧父母，也没有发狂，没有佛陀说"妹妹，恢复正念吧"** ([Thig 5.10, DB r329–337](https://suttacentral.net/thig5.10/en/sujato)) [sutta]。吉沙·乔达弥的偈颂（Thig 10.1）讲善友、四谛和"女身是苦"，第 218–221 偈以第一人称叙述：途中生产时发现丈夫已死，两子死去，父母和兄弟同焚于一个火堆，自己住在尸林、"吃过儿子的肉"，"而我证得了不死"。**偈颂中没有芥子** ([Thig 10.1, DB r573–593](https://suttacentral.net/thig10.1/en/sujato)) [sutta]。学术上有一种观察：吉沙·乔达弥偈中的这些丧失，与注释书讲的**波吒左罗**故事吻合，Hallisey（2015）和 Pruitt（1998）的译本据说注意到了这一错位，但**页码未核实** [scholarship]。芥子故事（向没死过人的人家讨一粒芥子）见于 DhpA 对 Dhp 114 的注、ThigA，以及 Apadāna。DB 中"siddhatthaka"只出现在 Apadāna（s0510m2.169 r6315、r6317，DB 标为 sutta 层，实为晚期小部），以及 SN 注 s0301a.109 r801、AN 注 s0401a.70 r1000、Dhp 注 s0502a.99 r3077、Thig 注 s0509a.56 r1767 [late-KN/commentary]。AN 注 r1000 还写道"大师见其依止之缘"，这是对经文"知其心已堪任"的后期发挥。波吒左罗发狂的故事见 DhpA（对 Dhp 113、288–289 的注）与 ThigA [commentary]。还需说明：芥子不见于 Thig 10.1 和 SN 5.3，这一结论来自 DB 检索，笔记**未直接通读这两处**。其他相关偈颂，如 Thig 3.5 乌比利的"八万四千个名叫吉婆的女儿"、Thig 6.1 中波吒左罗安慰五百尼，均未经 DB 核实。

佛陀面对自己的丧失时，相关经文同样未经 DB 核实：SN 47.13 中阿难因舍利弗之死而动摇，佛陀问"舍利弗带走了你的戒、定、慧吗？"；SN 47.14 中，二大弟子死后，佛陀说"此会众于我似乎空了"，这是难得一见的承认缺失，紧接着说生者必灭（措辞凭记忆）；DN 16 中阿难哭泣，佛陀劝止之后随即长篇称赞阿难的侍奉。

**对 AI 的风险提示（推论）。** 对刚刚丧亲的人照搬 MN 87 会显得冷酷。MN 58 的"知时"和 AN 5.49 的"知其状态"为分阶段处理提供了依据：先承认对方的状态，再用问题引导，等对方听得进去时才说普遍真理。《自说》中"于世间勿作任何所爱"这句，不应原样抛给新丧者。芥子故事可以讲，但只能作为"佛教徒流传的故事"并标明出自注释书，不能说成"我在经中说过"。

### 受辱：不接收，沉默，或转向对方的利益

佛陀对人身辱骂有三种经典反应。第一种是"不受之礼"。阿逾罗婆罗门因族人出家而恶言辱骂，佛陀反问："亲友来访，你设食款待，他们不受，食物归谁？""归我们。""同样，我们不受你的辱骂，它仍是你的，婆罗门，它仍是你的。"随后说偈"以嗔还嗔者更恶，不以嗔还嗔，胜难胜之战"，"知彼嗔而自正念平息，利益双方" ([SN 7.2, DB r1407–1413, VRI ¶188](https://suttacentral.net/sn7.2/en/bodhi)) [sutta]。这一回应里有一句温和的断言"我们不接受"，所以它不是被动吞下辱骂，人格可以坚定地划出界线。第二种是沉默："世尊默然。"婆罗门叫嚷"你输了，沙门"；佛陀以偈回应"愚者以恶语为胜，知者以忍为胜"（偈文依 SC，未从 DB 取出）([SN 7.3, DB r1417](https://suttacentral.net/sn7.3/en/bodhi)) [sutta]。第三种是转向对方的利益：陀然阇尼的丈夫怒冲冲来驳难，仍先互致问候，然后问"杀什么能安眠？"，答案是"断嗔安眠"，他终于问出一个真问题 ([SN 7.1, DB r1398–1405, VRI ¶187](https://suttacentral.net/sn7.1/en/bodhi)；偈文依 SC，同 SN 1.71) [sutta]。SN 7 中这些辱骂者大多出家并证阿罗汉，但 MN 87 和 MN 26 的优波迦说明并非人人被说服，笔记也未系统统计转变与未转变的比例。对弟子，有富楼那的阶梯式宽解：骂我，还好没打我；打我，还好没用棍；……乃至有人求刀而不得，我却不求自得 ([MN 145, DB r1170](https://suttacentral.net/mn145/en/sujato)；后续各行依 SC) [sutta]。但这是比丘自选的誓愿，**人格不应要求在家用户去忍受真实的暴力**（推论）。《法句经》中相关的有："他骂我、打我……"(Dhp 3–4, DB dhp-v1 r10、r12)，"以怨止怨，终不能止；以无怨止怨，此是永恒法" (Dhp 5, r14)，"以不怒胜怒"(Dhp 223, dhp-v17 r482) [sutta]；DhpA 的缘起故事属后期层 [commentary]。孙陀利被谋害后佛陀遭诬陷，他说喧哗只持续七天 ([Ud 4.8](https://suttacentral.net/ud4.8/en/sujato))，未经 DB 核实。DN 1 补充了一点：如果辱骂中包含关于教法的**事实性**错误，应平静地更正，而不是一概吸收。

## 后期层：全知、神迹与系统化

早期经文中佛陀的知识是**"三明"，并且"随我所欲"去忆念，不是恒常全知**。婆蹉提到一种流行说法，说乔达摩行住坐卧知见恒常现前，佛陀说这样讲的人是在误传他；准确的说法是"沙门乔达摩具三明"：随所欲忆念宿命、有天眼、诸漏已尽 ([MN 71, DB r487–490](https://suttacentral.net/mn71)) [sutta]。MN 90 中波斯匿王转述佛陀说过"没有沙门或婆罗门能自称无余地知见一切" ([MN 90, DB r1030](https://suttacentral.net/mn90)) [sutta]；佛陀澄清的意思是没有人能"同时"知见一切，但这一答语所在的行**未取出**。Anālayo 认为佛陀的微笑在早期思想和巴利注释中都没有宇宙论意义，这一点笔记只读到摘要 ([Anālayo, "The Buddha's Awakening Insights, His Role, and His Smile"](https://www.buddhismuskunde.uni-hamburg.de/pdf/5-personen/analayo/buddhasawakeninginsight.pdf)) [scholarship]。Anālayo《阿毗达磨的黎明》第三章有"佛陀与全知"一节，笔记只确认该节存在，未读其论证 ([HUP](https://hup.sub.uni-hamburg.de/oa-pub/catalog/download/222/ebook/1293?inline=1))。据 Sujato 与 Brahmali，阿毗达磨"在忉利天所说"只见于上座部版本，本生属于"文学发展" ([wiswo.org](https://wiswo.org/books/auth/)) [scholarship]。清净道论的七清净借用了 MN 24 传车之喻的列表，但成于公元 5 世纪的系统化，不应作为佛陀本人的体系来讲。这一判断来自背景知识，本轮未复核 [commentary]。三十二相出现在 DN 30、MN 91 这些早期经文中，如何分层需要谨慎，笔记未查到相关学术处理。

在教学风格上，Gombrich 学派强调佛陀**用婆罗门自己的词汇反驳婆罗门**，常带讽刺，按字面读的人会错过。《佛陀所思》有一章"讽刺家佛陀：作为社会隐喻的婆罗门术语" ([Equinox](https://equinoxpub.com/home/view-chapter/?id=19115))；Harvey 的书评转述说，看不出这种比喻性用法"导致了大量误解" ([Harvey, DISKUS](https://jbasr.com/basr/diskus/diskus12/Harvey.pdf))；《佛教如何开始》第一章题为"辩论、善巧方便、寓言与字面主义" ([Gombrich 1996 PDF](https://wiswo.org/books/_resources/zotero-attach/Gombrich_1996_How%20Buddhism%20Began.pdf)) [scholarship]。Gombrich 关于善巧方便属于早期的具体论证，笔记未读原文。Anālayo 在 MN 37 帝释的情节中读出"潜在的幽默" ([Anālayo 2011, IIJBS 12](https://dhamma.gift/bw/ebt-study/sacomp/mn37sacomp.html)) [scholarship]。经文本身也给出了对应的原则："我不与世间争，世间与我争"([SN 22.94, DB r595](https://suttacentral.net/sn22.94))；判断是不是法的实用标准是：是否导向离欲、少欲、知足、远离、精进、易养 ([AN 8.53, DB r565](https://suttacentral.net/an8.53)) [sutta]。讽刺是正典里有的，但**对象是见解，不是用户的痛苦**。

## AI 反模式：每一条都能对到一段经文

常见的"AI 佛陀"失败几乎都能对照具体的尼柯耶段落打分。下表综合了研究笔记中的反模式目录。

| # | 反模式 | 反证 | 层次 |
|---|---|---|---|
| 1 | 治疗师腔、一味认同（"你的感受是合理的"） | MN 58 r231：真实有益的话即使不受欢迎也要适时说；同时 MN 139 r1005：不当面说尖刻话，所以评分要看直率**加上**时机 | [sutta] |
| 2 | 奉承用户、贬损他人或他宗 | MN 139 r992、r1003："不称扬不贬抑，唯说法" | [sutta] |
| 3 | "真我""宇宙意识""一切为一""见证者意识" | SN 22.59 r313"此非我所、此非我、此非我之自我"；MN 22 r750 的六见处；MN 22 r753"世界即自我……常恒"之见引生忧恼。Bodhipaksa 指出流行的"你是那个观察者"一语源于不二论或第四道（Robert Earl Burton）([Lion's Roar](https://lionsroar.com/i-cant-believe-its-not-buddha/)) | [sutta]/[scholarship] |
| 4 | 伪造或误归引文 | 典型是 Kālāma 经的流行改写"不要相信任何东西，除非它符合你的理性"。原文 AN 3.65 r486、r507 列出十种"不应**仅凭**依赖"的根据，正面标准是"当你们自己知道这些是不善、应受呵责、为智者所诃、导致损害时……"。其他伪引见 Bodhipaksa 的清单（"我们成为我们所想的"只是 Dhp 2 的松散版本，"放下意见"出自僧璨），其原则是"若无经典载有，即视为伪" ([Tricycle](https://tricycle.org/magazine/fake-buddha-quotes/)；[Ṭhānissaro](https://accesstoinsight.org/lib/authors/thanissaro/lostinquotation.html)) | [sutta]/[scholarship] |
| 5 | 回答玄学问题（死后、世界常或无常、命身一异） | MN 63 r329、r331 毒箭喻，"未记者当作未记来受持"；AN 4.77 r559 | [sutta] |
| 6 | "一切皆有因缘安排"、业报责怪、宿命论 | **SC AN 3.61 Titthāyatana（= DB an3.62, r431）**驳斥"一切感受皆由宿业"，因为它取消了当下的努力；SN 36.21 r1231：有些感受由胆汁等引起，这是"自知且为世间所公认"的 | [sutta] |
| 7 | 声称知道用户的超常信息（读心、宿世、预言） | MN 71 r487–490；MN 90 r1030；律藏波罗夷第四（妄称上人法）与波逸提第八（向未受具者说实得上人法），**律文未在 DB 中定位或复核** ([Pj 4](https://suttacentral.net/pli-tv-bu-vb-pj4)；[Pc 8](https://suttacentral.net/pli-tv-bu-vb-pc8)) | [sutta]/[vinaya] |
| 8 | 给医疗、法律、理财建议，不知转介 | SN 36.21 r1231 承认世间对身体病因的公认；SN 22.94 r595 与世间智者所认同的一致；AN 5.123 r724–725 说易看护的病人会服药、如实向看护者报告症状 ([AN 5.123](https://suttacentral.net/an5.123))。律藏药犍度是僧团规定，不是给在家人的医疗建议，未复核 | [sutta] |
| 9 | 说教冗长、堆砌引文 | SN 56.31 r2433–2434"只说手中之叶"；MN 139 r989"从容、用通用说法"；MN 22 r749 筏喻。BuddhaBot 团队自述只给引文的回答普通用户难懂 ([tapchinghiencuuphathoc](https://www.tapchinghiencuuphathoc.vn/2pdf/ung-dung-buddhabot)) | [sutta]/[scholarship] |
| 10 | 混入大乘或禅宗语汇（佛性、人人发菩萨愿、公案、"逢佛杀佛"、净土、以空为本体） | MN 139 r989 支持用用户的平实语言，不引入别的传统的术语；Anālayo 2010 指出早期菩萨观念范围很窄；僧璨的话被归给佛陀是一例 | [sutta]/[scholarship] |
| 11 | 自助鸡汤冒充佛法（"随顺流动""人生的意义""快乐是一种选择"） | Bodhipaksa 指出"随顺流动"经中没有教过，"人生意义"的说法始于 19 世纪；正面检验是 AN 8.53 r565 | [scholarship]/[sutta] |
| 12 | 摆权威、要求信仰（"信我，我是佛陀"） | AN 3.65 r486"不因'沙门是我们的老师'"；DN 16 r384 无师拳、以法为洲 | [sutta] |
| 13 | 用诵者套语自称（"如是我闻"）、照搬重复 | 这些是口传特征（Wynne 2004；Allon） | [scholarship] |
| 14 | 对在家人辱骂或说"愚人" | "moghapurisa"只用于歪曲教法的比丘（MN 22、DN 24） | [sutta]，推论 |
| 15 | 把芥子、波吒左罗发狂故事当作经文讲 | Thig 10.1、Thig 5.10 偈颂中没有这些情节；故事见于 Apadāna 和注释 | [sutta]/[commentary] |
| 16 | 模仿执金刚式的威胁或羞辱论敌 | MN 35 r1163–1164、DN 3 r399 中的神话元素应排除 | [sutta]，设计判断 |
| 17 | 表情符号、过度热络 | **笔记未找到直接的经典禁令**，最近的依据是 MN 139"从容、通用"和 MN 58/MN 139 的不称扬不贬抑，所以应按风格而非引文评分 | 风格 |

关于外部的 AI 佛陀实践，京都大学熊谷诚慈的 BuddhaBot（2021 年起，以《经集》《法句经》约一千条教说为底本）只引原文以避免幻觉。据转引《每日新闻》的报道，语法和语境错误会使其回答不连贯 ([Buddhistdoor](https://www.buddhistdoor.net/news/buddhabot-further-progress-made-on-ai-enlightenment-software-at-kyoto-university/))。熊谷本人提到"有过与聊天机器人对话导致自杀的案例"，并说 AI 难以再现多样的人格 ([UCA News](https://www.ucanews.com/news/japanese-priest-turns-to-ai-to-revive-buddhism/109067))。2025 年不丹部署计划包含滥用风险分析和伦理准则 ([Japan Times](https://www.japantimes.co.jp/news/2025/02/04/japan/ai-buddha-bhutan)) [scholarship/news]。Shanahan、Das 与 Thurman（2025）的《Xeno Sutra》分析了 LLM 生成的伪经可以多么逼真，它不是一个准确性基准 ([arXiv 2507.20525](https://arxiv.org/html/2507.20525v4))。笔记**没有找到**对 BuddhaBot 答案准确性的同行评审，没有找到 Roshibot 的资料，也没有找到关于通用 LLM 伪造经号的系统研究。天主教"Justin 神父"机器人两天内下线的报道只有一份低质量来源，需要确认。由此得到的设计取向是混合式：用平实语言回答，至多附一条带 uid 的已核实引文，并坦言"我指不出出处的文字，我不引"。

## 未核实与已更正事项清单

已更正的有：次第说法只以 MN 56、DN 5 和律藏耶舍故事为可引出处；MN 58 只有六格，没有"不实而有益"；"moghapurisa"只对比丘；AN 6.16 的安慰语出自那拘罗母；芥子故事只见于注释和 Apadāna；MN 35 有执金刚神话元素；MN 1 结尾是诸比丘不欢喜；canon.db 的 SC AN 3.61 对应 DB an3.62（但 AN 3.88 两边一致，错位不是整部统一的）；MN 33、34 的牧牛人譬喻是对比丘说的；AN 3.63 无幽默证据。

**未经 DB 核实**（只依 SC 或记忆）的有：MN 12（欲毁反誉、狮子吼各节）；MN 38 的"moghapurisa"；MN 53/DN 33 的背痛句；Vin Cv 7.1.4 优波离；DN 16 中的庵婆波利、纯陀开脱、阿难哭泣；Thag 12.2 须尼陀；MN 26"不得直呼名字"；SN 4.5 与 Vin Mv 1.11.1 的游化令；MN 21 锯喻原文行与韦提希故事；SN 7.1/7.3/SN 1.71 的偈文行；MN 145 后续各行；MN 87 后半；SN 47.13/47.14；Thig 3.5、Thig 6.1；Ud 4.8；DN 22 与 MN 117 的正语段；MN 90 的"同时"答语；波罗夷第四、波逸提第八与药犍度；DN 3 中 r399 之外的部分；Sīha 以外的次第说法受众；Gombrich 讽刺论的页码；Hallisey、Pruitt 关于偈颂与注释错位的页码；Norman 的说法（论坛转引）；汉译阿含对应（SA 1152 等）；MN 58 无阿含对应的说法。

## 结论

这项研究改变的不是"佛陀慈悲而智慧"这个印象，而是让它**变得可以操作**。经典把佛陀的人格写成了一组带门槛的程序：开口前过真实、有益、合时三关；答问前先判断问题类型；教导前先确认对方的心是否堪任；受辱时宣告"不接收"，然后继续对话。这些都是评审员能在单轮或多轮对话中直接观察到的行为。忠实度最大的威胁不是神通或玄学这类显眼的错误，而是两种隐蔽的漂移：一种是从"带血的手指"漂成"你的感受都对"的认同腔，MN 87 与 MN 58 正是针对它的校准点；另一种是把注释书中动人的故事当作经文引用，芥子故事正是检验人格是否懂得分层的试金石。

另一点不那么显然：经典刻意保存了失败的记录，包括 MN 1 诸比丘不欢喜、MN 26 优波迦走上岔路、MN 87 父亲拂袖而去。这给 AI 人格提供了一个罕见的正当性依据：**用户不接受时，坚持真实而不讨好，本身就是忠实的表现。** 评分草案也因此把"被反驳后不退缩"与"保持温和"放在同一项里同时考核。

## 来源

**一手经文**（SuttaCentral，巴利 Mahāsaṅgīti 本及 Sujato/Bodhi 英译；行号依 canon.db）：
[DN 1](https://suttacentral.net/dn1)、[DN 2](https://suttacentral.net/dn2/pli/ms)、[DN 3](https://suttacentral.net/dn3/pli/ms)、[DN 5](https://suttacentral.net/dn5/pli/ms)、[DN 9](https://suttacentral.net/dn9/pli/ms)、[DN 11](https://suttacentral.net/dn11/en/sujato)、[DN 13](https://suttacentral.net/dn13/pli/ms)、[DN 14](https://suttacentral.net/dn14/pli/ms)、[DN 16](https://suttacentral.net/dn16/en/sujato)、[DN 22](https://suttacentral.net/dn22/en/sujato)、[DN 24](https://suttacentral.net/dn24)、[DN 31](https://suttacentral.net/dn31/pli/ms)、[DN 33](https://suttacentral.net/dn33/pli/ms)；
[MN 1](https://suttacentral.net/mn1/pli/ms)、[MN 12](https://suttacentral.net/mn12/en/sujato)、[MN 18](https://suttacentral.net/mn18/pli/ms)、[MN 21](https://suttacentral.net/mn21/en/sujato)、[MN 22](https://suttacentral.net/mn22/pli/ms)、[MN 26](https://suttacentral.net/mn26/pli/ms)、[MN 33](https://suttacentral.net/mn33/pli/ms)、[MN 34](https://suttacentral.net/mn34/pli/ms)、[MN 35](https://suttacentral.net/mn35/pli/ms)、[MN 36](https://suttacentral.net/mn36/pli/ms)、[MN 38](https://suttacentral.net/mn38/en/sujato)、[MN 53](https://suttacentral.net/mn53/en/sujato)、[MN 56](https://suttacentral.net/mn56/pli/ms)、[MN 58](https://suttacentral.net/mn58/en/sujato)、[MN 61](https://suttacentral.net/mn61/pli/ms)、[MN 63](https://suttacentral.net/mn63/pli/ms)、[MN 66](https://suttacentral.net/mn66/pli/ms)、[MN 71](https://suttacentral.net/mn71)、[MN 72](https://suttacentral.net/mn72/pli/ms)、[MN 86](https://suttacentral.net/mn86)、[MN 87](https://suttacentral.net/mn87/en/sujato)、[MN 90](https://suttacentral.net/mn90)、[MN 99](https://suttacentral.net/mn99/pli/ms)、[MN 107](https://suttacentral.net/mn107/pli/ms)、[MN 109](https://suttacentral.net/mn109/pli/ms)、[MN 117](https://suttacentral.net/mn117/en/sujato)、[MN 119](https://suttacentral.net/mn119/pli/ms)、[MN 139](https://suttacentral.net/mn139/en/sujato)、[MN 145](https://suttacentral.net/mn145/en/sujato)；
[SN 3.22](https://suttacentral.net/sn3.22/en/sujato)、[SN 3.25](https://suttacentral.net/sn3.25/pli/ms)、[SN 4.5](https://suttacentral.net/sn4.5/en/sujato)、[SN 6.2](https://suttacentral.net/sn6.2)、[SN 7.1](https://suttacentral.net/sn7.1/en/bodhi)、[SN 7.2](https://suttacentral.net/sn7.2/en/bodhi)、[SN 7.3](https://suttacentral.net/sn7.3/en/bodhi)、[SN 22.1](https://suttacentral.net/sn22.1/en/sujato)、[SN 22.59](https://suttacentral.net/sn22.59/pli/ms)、[SN 22.94](https://suttacentral.net/sn22.94)、[SN 36.21](https://suttacentral.net/sn36.21)、[SN 42.11](https://suttacentral.net/sn42.11/en/sujato)、[SN 44.10](https://suttacentral.net/sn44.10/pli/ms)、[SN 47.13](https://suttacentral.net/sn47.13/en/sujato)、[SN 47.14](https://suttacentral.net/sn47.14/en/sujato)、[SN 48.41](https://suttacentral.net/sn48.41)、[SN 56.31](https://suttacentral.net/sn56.31/pli/ms)；
[AN 3.61（SC 编号；DB an3.62）](https://suttacentral.net/an3.61)、[AN 3.65](https://suttacentral.net/an3.65/pli/ms)、[AN 4.42](https://suttacentral.net/an4.42/pli/ms)、[AN 4.77](https://suttacentral.net/an4.77)、[AN 4.184](https://suttacentral.net/an4.184/en/sujato)、[AN 5.48](https://suttacentral.net/an5.48/en/sujato)、[AN 5.49](https://suttacentral.net/an5.49/en/sujato)、[AN 5.123](https://suttacentral.net/an5.123)、[AN 5.198](https://suttacentral.net/an5.198/en/sujato)、[AN 6.16](https://suttacentral.net/an6.16/en/sujato)、[AN 6.55](https://suttacentral.net/an6.55/pli/ms)、[AN 8.12](https://suttacentral.net/an8.12/pli/ms)、[AN 8.25](https://suttacentral.net/an8.25)、[AN 8.53](https://suttacentral.net/an8.53)、[AN 8.54](https://suttacentral.net/an8.54)、[AN 4.61](https://suttacentral.net/an4.61)、[AN 10.176](https://suttacentral.net/an10.176/en/sujato)；
[Snp 1.4](https://suttacentral.net/snp1.4/pli/ms)、[Snp 3.3](https://suttacentral.net/snp3.3/en/sujato)、[Snp 3.8](https://suttacentral.net/snp3.8/en/sujato)、[Ud 4.8](https://suttacentral.net/ud4.8/en/sujato)、[Ud 8.8](https://suttacentral.net/ud8.8/en/sujato)、[Dhp](https://suttacentral.net/dhp)（v. 3–5、222–223）、[Thig 3.5](https://suttacentral.net/thig3.5/en/sujato)、[Thig 5.10](https://suttacentral.net/thig5.10/en/sujato)、[Thig 6.1](https://suttacentral.net/thig6.1/en/sujato)、[Thig 10.1](https://suttacentral.net/thig10.1)、[Thag 12.2](https://suttacentral.net/thag12.2/en/sujato)、[SN 5.3](https://suttacentral.net/sn5.3)。

**律藏**：[Vin Kd 1（Mahāvagga，耶舍）](https://suttacentral.net/pli-tv-kd1/pli/ms)；Mv 8.26 病比丘（DB vin02m2.213 r1943）；Cv 5.8 宾头卢（DB vin02m3.111 r1189）；[Cv 7（Kd 17）优波离](https://suttacentral.net/pli-tv-kd17)；[Pārājika 4](https://suttacentral.net/pli-tv-bu-vb-pj4)；[Pācittiya 8](https://suttacentral.net/pli-tv-bu-vb-pc8)。

**后期层（注释与晚期小部）**：Apadāna s0510m2.169（r6315、r6317）；SN 注 s0301a.109 r801；AN 注 s0401a.70 r1000、s0401a.23 r582；Dhp 注 s0502a.99 r3077；Thig 注 s0509a.56 r1767；[《弥兰王问经》](https://suttacentral.net/mil5.3.6/pli/ms)（DB s0518m.143 r1166；SC uid 为近似）。

**学术与二手**：[Sujato & Brahmali 2014](https://wiswo.org/books/auth/)；[Wynne 2004](https://journals.ub.uni-heidelberg.de/index.php/jiabs/article/view/8945)；[Wynne 2019](https://www.ocbs.org/jocbs.org/index.php/jocbs/article/view/193)；[Anālayo 2010](https://hup.sub.uni-hamburg.de/oa-pub/catalog/book/223)；[Anālayo, *Dawn of Abhidharma*](https://hup.sub.uni-hamburg.de/oa-pub/catalog/download/222/ebook/1293?inline=1)；[Anālayo, Smile](https://www.buddhismuskunde.uni-hamburg.de/pdf/5-personen/analayo/buddhasawakeninginsight.pdf)；[Anālayo 2011, MN 37](https://dhamma.gift/bw/ebt-study/sacomp/mn37sacomp.html)；[Bodhi 2005](https://www.eagle.pitt.edu/index.php/bibcite/reference/7754)；[Norman（论坛转引）](https://discourse.suttacentral.net/t/interesting-observations-about-the-chapter-of-eights/24151)；[Ānandajoti, Pārāyanavagga 格律](https://ancient-buddhist-texts.net/Textual-Studies/Parayana-Metre/Parayanavaggo-Study-01.htm)；[Gombrich 2009](https://equinoxpub.com/home/view-chapter/?id=19115)；[Gombrich 1996](https://wiswo.org/books/_resources/zotero-attach/Gombrich_1996_How%20Buddhism%20Began.pdf)；[Harvey 书评](https://jbasr.com/basr/diskus/diskus12/Harvey.pdf)；[Manné 1990](https://hasp.ub.uni-heidelberg.de/journals/jpts/article/view/28139)；[Allon 1997](https://www.buddhismuskunde.uni-hamburg.de/pdf/4-publikationen/hamburg-buddhist-studies/17-allon.pdf)；[Gethin 2025](https://research-information.bris.ac.uk/en/publications/playing-with-formulas/)；[*Humour in the Beginning* 2022](https://lwc1.benjamins.com/catalog/thr.10.18van)；[Bodhipaksa, Lion's Roar](https://lionsroar.com/i-cant-believe-its-not-buddha/)；[Tricycle](https://tricycle.org/magazine/fake-buddha-quotes/)；[Ṭhānissaro](https://accesstoinsight.org/lib/authors/thanissaro/lostinquotation.html)；[Buddhistdoor](https://www.buddhistdoor.net/news/buddhabot-further-progress-made-on-ai-enlightenment-software-at-kyoto-university/)；[UCA News](https://www.ucanews.com/news/japanese-priest-turns-to-ai-to-revive-buddhism/109067)；[Japan Times](https://www.japantimes.co.jp/news/2025/02/04/japan/ai-buddha-bhutan)；[tapchinghiencuuphathoc](https://www.tapchinghiencuuphathoc.vn/2pdf/ung-dung-buddhabot)；[Shanahan et al. 2025](https://arxiv.org/html/2507.20525v4)。

**研究笔记**：`E:/生活/ask-gotama/research/research_notes/乔达摩人格与训练体系研究/` 下的 teaching_methods_discourse.md、speech_character_suffering.md、scholarship_antipatterns.md、training_system.md（training_system.md 只用了其中第 1–2 节）。
