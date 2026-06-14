# Awesome Thai library [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> รวบรวมไลบราลี่ เครื่องมือ โมเดล และชุดข้อมูลต่าง ๆ สำหรับการทำงานกับภาษาไทย
>
> A curated list of libraries, tools, models, and datasets for working with the Thai language. 🇹🇭

## Contents

- [NLP Toolkits](#nlp-toolkits)
- [Word & Syllable Segmentation](#word--syllable-segmentation)
- [Language Models (LLMs)](#language-models-llms)
- [Speech (ASR / TTS)](#speech-asr--tts)
- [OCR](#ocr)
- [Datasets & Corpora](#datasets--corpora)
- [Evaluation & Benchmarks](#evaluation--benchmarks)
- [Address & Geography](#address--geography)
- [ID & Tax Validation](#id--tax-validation)
- [Payments (PromptPay)](#payments-promptpay)
- [Finance & Banking](#finance--banking)
- [Date & Buddhist Calendar](#date--buddhist-calendar)
- [Number & Baht Text](#number--baht-text)
- [Fonts](#fonts)
- [Others](#others)
- [Tools](#tools)
- [Related Lists](#related-lists)

## NLP Toolkits
#### ชุดเครื่องมือประมวลผลภาษาไทยแบบครบวงจร

- [PyThaiNLP](https://github.com/PyThaiNLP/pythainlp) `[Python]` ชุดเครื่องมือ NLP ภาษาไทยครบวงจร — ตัดคำ, POS, NER, romanize, สะกดคำ, แปลงเลข/วันที่ (de-facto Thai NLP toolkit)
- [TLTK](https://pypi.org/project/tltk/) `[Python]` Thai Language Toolkit — ตัดคำ/ตัดพยางค์/ถอดเสียง (g2p) โดย รศ.ดร.วิโรจน์ อรุณมานะกุล
- [nlpO3](https://github.com/PyThaiNLP/nlpo3) `[Rust]` ไลบรารี NLP ภาษาไทยเขียนด้วย Rust เน้นความเร็ว มี binding สำหรับ Python และ Node.js
- [Thai-NNER](https://github.com/vistec-AI/Thai-NNER) `[Python]` โมเดลรู้จำชื่อเฉพาะแบบซ้อน (nested NER) สำหรับภาษาไทย โดย VISTEC
- [Han-Coref](https://github.com/PyThaiNLP/han-coref) `[Python]` โมเดลแก้การอ้างถึง (coreference resolution) ภาษาไทย

## Word & Syllable Segmentation
#### library สำหรับตัดคำและตัดพยางค์ภาษาไทย

- [libthai](https://linux.thai.net/projects/libthai) linux package สำหรับจัดการกับภาษาไทย
- [Wordcut](https://github.com/veer66/wordcut) `[Node.js]` ตัดคำไทย
- [AttaCut](https://github.com/PyThaiNLP/attacut) `[Python]` ตัดคำไทยด้วย CNN เร็วกว่า DeepCut ~6 เท่า
- [DeepCut](https://github.com/rkcosmos/deepcut) `[Python]` ตัดคำไทยด้วย Convolutional Neural Networks
- [CutKum](https://github.com/pucktada/cutkum) `[Python]` ตัดคำไทยด้วย RNN-LSTM บน tensorflow
- [SEFR CUT](https://github.com/mrpeerat/SEFR_CUT) `[Python]` ตัดคำไทยแบบ Stacked Ensemble รองรับการปรับโดเมน (EMNLP 2020)
- [OSKut](https://github.com/mrpeerat/OSKut) `[Python]` ตัดคำไทยที่ทนต่อข้อมูลนอกโดเมน (ACL 2021 Findings)
- [ssg](https://github.com/ponrawee/ssg) `[Python]` ตัดพยางค์ภาษาไทยด้วย CRF
- [PhlongTaIam](https://github.com/veer66/PhlongTaIam) `[PHP]` ตัดคำไทย
- [thsplitlib](https://github.com/moohooooo/thsplitlib) `[PHP]` ตัดคำไทย
- [lexto](https://github.com/telember/lexto) ตัดคำไทย
- [pythaiwordcut](https://github.com/narongdejsrn/pythaiwordcut) `[Python]` ตัดคำภาษาไทย Maximum Matching algorithm
- [jtcc](https://github.com/wittawatj/jtcc) ตัดกลุ่มตัวอักษร (TCC) ตามกฎภาษาไทย

## Language Models (LLMs)
#### โมเดลภาษาไทยขนาดใหญ่และโมเดลภาษาแบบ pretrained

- [Typhoon](https://opentyphoon.ai) ([HF](https://huggingface.co/scb10x)) โมเดลภาษาไทยขนาดใหญ่โดย SCB 10X — รุ่นปัจจุบัน Typhoon 2 / 2.1 ครอบคลุมสนทนา การให้เหตุผล เสียง และภาพ
- [OpenThaiGPT](https://github.com/OpenThaiGPT/openthaigpt) ([HF](https://huggingface.co/openthaigpt)) โมเดลภาษาไทยแบบโอเพนซอร์ส (7B–72B + รุ่นคิดวิเคราะห์ R1) โดยสมาคม AIEAT
- [Pathumma / OpenThaiLLM](https://huggingface.co/nectec) ([GitHub](https://github.com/nectec)) โมเดลภาษาไทยระดับชาติโดย NECTEC (สวทช.) — ตระกูล "ปทุมมา" รองรับข้อความ ภาพ และเสียง
- [WangchanBERTa / thai2transformers](https://github.com/vistec-AI/thai2transformers) โมเดลภาษาไทยแบบ Transformer (RoBERTa) โดย VISTEC-depa AIResearch
- [WangchanX](https://github.com/vistec-AI/WangchanX) เฟรมเวิร์ก/สูตรสำหรับ fine-tune โมเดลภาษาไทยโดย VISTEC
- [WangchanLion](https://github.com/vistec-AI/WangchanLion) โมเดลภาษาไทยแบบ instruction-tuned (ต่อยอดจาก SEA-LION)
- [WangChanGLM](https://github.com/PyThaiNLP/WangChanGLM) โมเดลภาษาไทยเชิงกำเนิดแบบ multilingual instruction-tuned
- [thai2fit](https://github.com/cstorm125/thai2fit) `[Python]` โมเดลภาษาไทย ULMFiT และเวกเตอร์คำ
- [SEA-LION](https://github.com/aisingapore/sealion) ([HF](https://huggingface.co/aisingapore)) โมเดลภาษาเอเชียตะวันออกเฉียงใต้ (รวมภาษาไทย) โดย AI Singapore
- [SeaLLMs](https://github.com/DAMO-NLP-SG/DAMO-SeaLLMs) ([HF](https://huggingface.co/SeaLLMs)) โมเดลภาษา SEA รวมภาษาไทย โดย Alibaba DAMO Academy
- [Sailor / Sailor2](https://github.com/sail-sg/sailor2) ([HF](https://huggingface.co/sail)) โมเดลภาษา SEA (Qwen-based) รวมภาษาไทย โดย Sea AI Lab

## Speech (ASR / TTS)
#### รู้จำเสียงพูดและสังเคราะห์เสียงภาษาไทย

- [Thonburian Whisper](https://github.com/biodatlab/thonburian-whisper) `[Python]` โมเดลรู้จำเสียงพูด (ASR) ภาษาไทยบนพื้นฐาน Whisper
- [wav2vec2-large-xlsr-53-th](https://huggingface.co/airesearch/wav2vec2-large-xlsr-53-th) โมเดล ASR ภาษาไทยโดย AIResearch
- [Pathumma Audio / F5-TTS](https://huggingface.co/nectec) โมเดลด้านเสียงและสังเคราะห์เสียงภาษาไทยโดย NECTEC (สวทช.)

## OCR
#### อ่านตัวอักษรภาษาไทยจากภาพ

- [EasyOCR](https://github.com/JaidedAI/EasyOCR) `[Python]` OCR หลายภาษารวมถึงภาษาไทย ใช้งานง่าย
- [Typhoon OCR](https://github.com/scb-10x/typhoon-ocr) `[Python]` OCR ภาษาไทยด้วยโมเดล Typhoon โดย SCB 10X
- [Thai-TrOCR](https://huggingface.co/openthaigpt/thai-trocr) โมเดล OCR ภาษาไทยแบบ TrOCR โดย OpenThaiGPT

## Datasets & Corpora
#### ชุดข้อมูลและคลังข้อความภาษาไทย

- [data.go.th](https://data.go.th/Datasets.aspx) ข้อมูลจากหน่วยงานรัฐ รวมทั้งข้อมูลทางสถิติ
- [Best I Corpus](https://www.nectec.or.th/corpus/index.php?league=pm) Corpus จาก Nectec
- [HSE Corpus](http://web-corpora.net/ThaiCorpus/) รวบรวมและจัดทำขึ้นโดย HSE School of Linguistics จากประเทศรัสเซีย
- [Wisesight Sentiment](https://github.com/PyThaiNLP/wisesight-sentiment) ชุดข้อมูลวิเคราะห์ความรู้สึก (sentiment) ภาษาไทยจากโซเชียลมีเดีย 26,737 ข้อความ (CC0)
- [prachathai-67k](https://github.com/PyThaiNLP/prachathai-67k) ชุดข้อมูลบทความข่าวภาษาไทยกว่า 67,000 บทความ
- [scb-mt-en-th-2020](https://huggingface.co/datasets/airesearch/scb_mt_enth_2020) ชุดข้อมูลแปลอังกฤษ-ไทยขนาดใหญ่โดย AIResearch/SCB
- [Thai-NNER dataset](https://github.com/vistec-AI/Thai-NNER) ชุดข้อมูล nested NER ภาษาไทยชุดแรก 104 ประเภท entity (ACL 2022)
- [Thai-NER](https://github.com/PyThaiNLP/Thai-NER) ชุดข้อมูลและโมเดล NER ภาษาไทยโดย PyThaiNLP
- [iApp Wiki QA](https://github.com/iapp-technology/iapp-wiki-qa-dataset) ชุดข้อมูลถาม-ตอบภาษาไทยจาก Wikipedia โดย iApp Technology
- [classification-benchmarks](https://github.com/PyThaiNLP/classification-benchmarks) รวม benchmark จำแนกข้อความภาษาไทย (Wisesight, Wongnai, Prachathai, TrueVoice)
- [SEACrowd](https://github.com/SEACrowd/seacrowd-datahub) ศูนย์รวมชุดข้อมูล NLP ภาษาเอเชียตะวันออกเฉียงใต้ (รวมภาษาไทย)
- [Thai-zip-geolocation](https://github.com/rathpanyowat/Thai-zip-code-latitude-and-longitude) พิกัดละติจูด ลองจิจูด ของรหัสไปรษณีย์
- [Thailand-Address](https://github.com/Cerberus/Thailand-Address) ข้อมูลที่อยู่ sql, json
- [Thai CG Bank](https://github.com/crishoj/thcg)
- [พจนานุกรม](https://raw.githubusercontent.com/korakot/thainlp/master/royin_dict_2542.tsv) ใช้ข้อมูลจาก [e4thai](http://www.e4thai.com/e4e/images/program/royal_thai_dictionary_2542.zip)
- [word dic](https://gist.github.com/anonymous/36568e5aaa73790e718757ff5f481afe)

## Evaluation & Benchmarks
#### ชุดประเมินความสามารถของโมเดลภาษาไทย

- [NitiBench](https://github.com/vistec-AI/nitibench) benchmark สำหรับงานถาม-ตอบกฎหมายไทย (คดีภาษี/กฎหมายแรงงาน) โดย VISTEC
- [Chinda-Eval](https://github.com/iapp-technology/chinda-eval) แพลตฟอร์มประเมิน LLM ภาษาไทยแบบครบวงจร (สร้างบน EvalScope) โดย iApp Technology
- [WangchanX-Eval](https://github.com/vistec-AI/WangchanX-Eval) ระบบประเมินการอ่านจับใจความ (MRC) ภาษาไทยโดยใช้ LLM เป็น judge
- [Thai-Sentence-Vector-Benchmark](https://github.com/mrpeerat/Thai-Sentence-Vector-Benchmark) ชุดข้อมูลเปรียบเทียบโมเดล sentence embedding ภาษาไทย

## Address & Geography
#### ข้อมูลและไลบรารีที่อยู่ จังหวัด/อำเภอ/ตำบล รหัสไปรษณีย์

- [jquery.Thailand.js](https://github.com/earthchie/jquery.Thailand.js) `[JS]` ตัวช่วยกรอกที่อยู่ไทยแบบ Auto Complete โดยไม่ต้องใช้ Server Side
- [thai-address-universal](https://github.com/ophoomo/thai-address-universal) `[TypeScript]` ไลบรารีที่อยู่ไทย รองรับทั้ง Node และเบราว์เซอร์ (เขียนใหม่จาก thai-address-database)
- [thailand-geography-json](https://github.com/thailand-geography-data/thailand-geography-json) ข้อมูล JSON จังหวัด/อำเภอ/ตำบล/รหัสไปรษณีย์
- [geothai](https://github.com/GeoThai/npm-packages) `[JS]` แพ็กเกจเข้าถึงข้อมูลภูมิศาสตร์ไทยแบบละเอียด
- [thai-address-database](https://github.com/Sellsuki/thai-address-database) `[JS]` ฐานข้อมูลที่อยู่ไทยฝั่ง client พร้อมค้นหาจังหวัด/อำเภอ/รหัสไปรษณีย์
- [react-thailand-address-typeahead](https://github.com/zapkub/react-thailand-address-typeahead) `[React]` คอมโพเนนต์ autocomplete ที่อยู่ไทย
- [thai-data](https://github.com/niawjunior/thai-data) `[JS]` ข้อมูลตำบล/อำเภอ/จังหวัด (77 จังหวัด) อ้างอิงรหัสไปรษณีย์ โดยไม่ใช้ server
- [thailand_gis](https://github.com/prasertcbs/thailand_gis) แผนที่ประเทศไทย (shapefile) แยกจังหวัด/อำเภอ/ตำบล

## ID & Tax Validation
#### ตรวจสอบเลขบัตรประชาชนและเลขประจำตัวผู้เสียภาษี

- [Thai-Citizen-ID-Validator](https://github.com/codeforthailand/Thai-Citizen-ID-Validator) `[JS]` ตรวจสอบเลขบัตรประชาชน
- [ThaiNationalIDCard](https://github.com/chakphanu/ThaiNationalIDCard) อ่านบัตรประชาชน
- [thai-citizen-id-validation-php](https://github.com/farzai/thai-citizen-id-validation-php) `[PHP]` ตรวจสอบและสุ่มเลขบัตรประชาชน
- [thai-citizen-id-validator-go](https://github.com/jukbot/thai-citizen-id-validator-go) `[Go]` ตรวจสอบเลขบัตรประชาชน
- [thai_citizen_id](https://pub.dev/packages/thai_citizen_id) `[Dart]` ตรวจสอบและจัดรูปแบบเลขบัตรประชาชน

## Payments (PromptPay)
#### สร้างและถอดรหัส QR พร้อมเพย์

- [promptparse](https://github.com/maythiwat/promptparse) `[TypeScript]` สร้างและถอดรหัส QR พร้อมเพย์/EMVCo (เบอร์โทร, บัตร ปชช., e-wallet, bill payment)
- [promptpay-qr](https://github.com/dtinth/promptpay-qr) `[JS]` สร้าง payload QR พร้อมเพย์ที่ถูกอ้างอิงมากที่สุด
- [promptpay-qr-php](https://github.com/farzai/promptpay-qr-php) `[PHP]` สร้าง QR พร้อมเพย์
- [promptparse-go](https://github.com/sirilerklab/promptparse-go) `[Go]` สร้าง/ถอดรหัส QR พร้อมเพย์/EMVCo
- [pypromptpay](https://github.com/wannaphong/pypromptpay) `[Python]` สร้าง QR Code พร้อมเพย์

## Finance & Banking
#### ธนาคาร สลิป และตลาดหุ้นไทย

- [thanakan](https://github.com/codustry/thanakan) `[Python]` อินเทอร์เฟซเชื่อมต่อ API ธนาคารไทย (KBANK, SCB) พร้อมตรวจสอบสลิป
- [slipverify](https://github.com/maythiwat/slipverify) `[TypeScript]` SDK ตรวจสอบสลิปโอนเงินธนาคาร/e-wallet ไทยจาก QR
- [ezyquant](https://github.com/ezyquant/ezyquant) `[Python]` ไลบรารี backtesting หุ้นไทย (SET) แบบ Pythonic

## Date & Buddhist Calendar
#### วันที่และปฏิทินพุทธศักราช

- [thaidate](https://pypi.org/project/thaidate/) `[Python]` แปลงและแสดงวันที่แบบพุทธศักราช
- [rundiz/thai-date](https://packagist.org/packages/rundiz/thai-date) `[PHP]` แสดงวันที่เป็นภาษาไทยคล้าย `date()`/`strftime()`
- [phattarachai/thaidate](https://packagist.org/packages/phattarachai/thaidate) `[PHP/Laravel]` ฟังก์ชัน `thaidate()` จัดรูปแบบวันที่ไทยพร้อมปี พ.ศ.
- [thai_buddhist_date](https://pub.dev/packages/thai_buddhist_date) `[Dart]` แปลงและจัดรูปแบบวันที่ พ.ศ.
- [thai_lunar](https://pub.dev/packages/thai_lunar) `[Dart]` ปฏิทินจันทรคติไทย รองรับปีอธิกมาส/อธิกวาร

## Number & Baht Text
#### แปลงตัวเลขเป็นคำอ่านและจำนวนเงินบาทไทย

- [ThaiBahtText](https://github.com/greatfriends/ThaiBahtText) `[.NET]` แปลงเงินจากตัวเลขเป็นคำอ่าน
- [bahttext](https://github.com/jojoee/bahttext) `[JS]` แปลงตัวเลขเป็นคำอ่านเงินบาท เลียนแบบ Excel BAHTTEXT()
- [thai-baht-text](https://github.com/antronic/thai-baht-text-js) `[TypeScript]` แปลงตัวเลขเป็นข้อความเงินบาทไทย แบบ zero-dependency
- [bahttext (Python)](https://pypi.org/project/bahttext/) `[Python]` แปลงจำนวนเงินเป็นข้อความเงินบาทไทย
- [AnuchitO/bahttext](https://github.com/AnuchitO/bahttext) `[Go]` แปลงเงินบาทเป็นข้อความ
- [thainum](https://pub.dev/packages/thainum) `[Dart]` ตัวเลขไทย, แปลงเลขเป็นคำ, baht text, วันที่/เวลาไทย

## Fonts
#### ฟอนต์ไทยและตัวช่วยจัดบรรทัด

- [Fontsource (Thai)](https://github.com/fontsource/fontsource) self-host ฟอนต์ไทยโอเพนซอร์สผ่าน npm (`@fontsource/sarabun`, `kanit`, `prompt`, `noto-sans-thai`, ฯลฯ)
- [@ibm/plex-sans-thai](https://www.npmjs.com/package/@ibm/plex-sans-thai) ฟอนต์ Plex Sans Thai อย่างเป็นทางการจาก IBM (looped + non-looped)

## Others
#### เครื่องมือไทยอื่น ๆ ที่ไม่จำกัดเฉพาะด้านภาษา

- [PDPA-Consent](https://github.com/iamapinan/PDPA-Consent) `[WordPress]` ปลั๊กอินขอความยินยอมตาม พ.ร.บ. คุ้มครองข้อมูลส่วนบุคคล (PDPA)
- [easylist-thailand](https://github.com/easylist-thailand/easylist-thailand) รายการกรองโฆษณา (adblock) สำหรับเว็บไซต์ไทย
- [howtotax](https://github.com/taepras/howtotax) เครื่องมือแสดงภาพการคำนวณภาษีเงินได้บุคคลธรรมดาแบบขั้นบันได
- [covidthailand](https://github.com/djay/covidthailand) รวมและเผยแพร่ข้อมูลโควิด-19 ของประเทศไทยจากหลายแหล่ง

## Tools
#### เครื่องมือและบริการอื่น ๆ

- [Nectec Innovation](https://www.nectec.or.th/innovation/innovation-software/)
- [ภาษีไปไหน](https://govspending.data.go.th) ระบบข้อมูลการใช้จ่ายภาครัฐ

## Related Lists
#### รายการ awesome อื่น ๆ ที่เกี่ยวข้อง

- [awesome-thai-dev](https://github.com/unnawut/awesome-thai-dev) รวมไลบรารี บทความ และทรัพยากรสำหรับนักพัฒนาภาษาไทย
