# FarsiQuAD-Dataset
 Farsi Question And Answer Dataset

Fast and accurate answers to the questions asked in natural language is one of the important goals in the development of question and answer systems in which the computer understands a context and question and provides the exact answer to the user. Although there has been a lot of progress in this area, it is still among the issues that need to be improved, especially for languages other than English, such as Persian. FarsiQuAD (FarsiQuAD) was created by humans from Persian Wikipedia articles and published in two versions. Version 1 contains 10,000+ questions and answers and version 2 contains a collection of over 145,000+ rows. This database has the ability to integrate with the English version of SQuAD and other databases of other languages that have used this standard. The results of this research show that the created Persian language question and answer database can provide the user with the answer to the questions asked in the natural Persian language with an exact matching criterion of 78%  and an F1 criterion of 87%, and it still needs to be improved.

# Data preparation and cleaning

The articles whose number of characters were between 500 and 1100 characters were extracted, and then pre-processing operations related to cleaning and sorting and data normalization were done using the digest library.

# Creating a program to facilitate the creation of questions

In order to collect questions, a strong, fast and user-friendly user interface was needed so that the required questions could be easily extracted, so for this purpose, the following software was created. The name of this software was named QAProject (Question Selection for Papers).

# Preparation of questions

Sample of the Article, Question And Answer:
" یغوارد (به ارمنی: ԵՂՎԱՐԴ) یک شهر در غرب ارمنستان است که در استان کوتایک واقع شده است. در کیلومتری شمال هرازدان، مرکز استان کوتایک واقع شده است. کلمه یغوارد از دو کلمه ارمنی یغی () به معنی (عطر یا بو) و وارد () به معنی (گل رز) مشتق شده است. به عقیده آرام غانالانیان پژوهشگر و ارمنی شناس نامگذاری یغوارد به دلیل وجود یک جنگل وسیع در این منطقه است که از انواع گل رز و سایر گل‌های با عطر زیاد پوشیده شده است یغوارد از کهن‌ترین اقامتگاه‌های بشری در منطقه است و در آن آثار معماری زیادی یافت می‌شود. یغوارد ۷ کیلومتر مربع مساحت دارد. یغوارد در جنوب کوه آرایی در ارتفاع ۱۳۳۳ متری از سطح دریا واقع شده است. این شهر در ۱۵ کیلومتری ایروان پایتخت جمهوری ارمنستان قرار گرفته است کلیسای یغوارد بنا شده در ۱۳۰۱ تنها بنای حفظ شده تاریخی در یغوارد می‌باشد. اف سی یغوارد یک باشگاه فوتبال بود و نماینده این شهرک در بین سال‌های ۱۹۸۶ تا ۱۹۹۶ بود و به دلایل مشکلات مالی منحل شد.
سوال 1: یغوارد در کدام کشور قرار دارد؟ ارمنستان
سوال2: شهر یغوارد در کدام قسمت از ارمنستان واقع است؟ غرب 
سوال 3: شهر یغوارد در کدام استان قرار دارد؟ پاسخ: کوتایک
سوال 4: یغوارد چقدر مساحت دارد؟ پاسخ: ۷ کیلومتر مربع
سوال 5: شهر یغوارد در چه فاصله ای از ایروان واقع است؟ پاسخ: ۱۵ کیلومتری"

The total number of extracted questions is more than 10,000 pairs of questions and answers, which are extracted from the text by comprehension and conceptually. In this set of questions, it has been carefully noted that the answer to the question must be extractable from the text, and for the questions that the system must know that it does not know the answer to, 153 questions have been recorded in version 1; Therefore, the number of questions containing answers is 9847 pairs in Version 1.

In this data, the lowest number of questions extracted from the articles is 1, the highest number of questions extracted from the article is 12, and the average question extracted from each article is 3.7.

##Things that have been observed in the preparation of questions:

- In choosing the answer, try to choose the lowest possible answer.

- In preparing answers with prefixes such as Ms., Mr., Haji, Engineer, General, etc., they are selected as part of the answer.

- Prefixes such as year, city, etc., if they were in the text of the question, are not considered in the answer.

- Suffixes such as meter, milliliter, kilometer, a million, lunar, solar, millimeter, etc. are also considered part of the answer, if these words are not present in the text of the question itself.

- Words that express approximations such as approximately, approximately, more than close to and... if they are not mentioned in the question, they are considered as part of the answer in the answer.

- Full reflection of the text used in the quotation.
In extracting, it has been tried to use different types of questions, including possessive, time, why, where, what, how, how, why, which, etc.

- In preparing the questions, questions with several connections have been used, for example, in the question it is said "What is the occupation of the father of the author of the article?", while in the text of the article, the name of the person is mentioned and the person's father is mentioned, and then the occupation of his father is discussed.

- Conditional questions have also been extracted, such as the question "Is Iran Khodro company public or private?".

- Equivalent words or concepts that are not exactly used in the text have been used repeatedly in preparing questions.

- In preparing the questions, both in the text of the question and in the answer to the question, words other than Persian were also used. For example, the question "Which family does hyacinth belong to?" Answer: "Hyacinthaceae".

- In its questions and answers, the written equivalent of Persian numbers and its opposite are used, such as (three, two, one, etc.)
In the design of the questions, care has been taken to ensure that each question can only be extracted from one article and that the probability of having an answer in other articles is very low.



