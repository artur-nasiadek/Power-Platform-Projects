## Foreign Words Dictionary w/ Power Apps, Power Automate, Dataverse

<h4>With this app the users can build and manage their own dictionary of foreign language words they would like to learn. The user enters a foreign word, its meaning, cases of use and records pronunciation. Twice a day a 'daily task' notification is sent to remind the user to practice the words.
All data is stored in a Dataverse table.</h4>
<br>

<h3>Walkthrough of the app</h3>

After opening the app the list of preselected foreign languages is displayed. User chooses the language to practice with.
<br>

<p><b>List of languages screen</b></p>
<img src="/Foreign Words Dictionary/Images/WelcomeScreen.jpg" width="200">

On the next screen a menu is displayed. User can add a new word, browse the list of already provided words, do a 'daily task', or transcript a word (speech-to-text feature). The flag in the screen's background indicates the chosen language.

<p><b>Menu screen</b></p>
<img src="/Foreign Words Dictionary/Images/MenuScreen.jpg" width="200">
<br>

<p><b>Add new word</b><p>
<p>In order to add a new word the user has to choose the 'base word' language, that is language the user already speaks. Then a base word has to be entered, and next the meaning (translation) in the chosen language to learn. The field 'Additional information' is optional, but here some use cases of the new word can be provided. Instead of entering the translation and use cases manually, the user can utilize AI by clicking on www icon in the top-right corner of the screen. It runs a Power Automate flow that prompts DeepSeek and populates output in the 'Translation' and 'Additional information' fields.
There is also the option to record pronunciation of the new word.</p>

<img src="/Foreign Words Dictionary/Images/AddNewWordScreen.jpg" width="200">
<br>

<p><b>Browse</b><p>
<p>Here the user can browse the list of words and translations, and access a selected word's card.</p>

<img src="/Foreign Words Dictionary/Images/BrowseScreen.jpg" width="200">
<br>

<img src="/Foreign Words Dictionary/Images/WordScreen.jpg" width="200">
<br>

In the word's card user has options to edit provided data or delete the word from the database.

<p><b>Daily task</b><p>
<p>On this screen the user can practice and exercise to learn foreign words by providing memorized translation of the base word. The app displays the words from newest to oldest. User checks provided translation against the one in the database, can mark it as correct or hide the word. If the word is marked as correct it will not be shown again until the whole list is completed. Hidden words can be shown again only by editting and setting the option 'unhide' in the given word's card. There is no set number of words to be shown in the daily task. The user decides when to stop the task. When the last word in the database is reached, the app starts to show the words from the beginning.
A scheduled Power Automate flow is used to send a notification to the user as a reminder about the daily task.</p>

<img src="/Foreign Words Dictionary/Images/DailyTaskScreen.jpg" width="200">
<br>

<img src="/Foreign Words Dictionary/Images/DailyTaskCheckScreen.jpg" width="200">
<br>

The toggle in the header of the screen gives the user an option to switch the base word with the translation, so the user can translate in the 'opposite direction'.

<p><b>Transcript word</b><p>
<p>Here the user can utilize speech-to-text feature. The transcribed word is added to the list and saved in the Dataverse. By clicking a word in the list the 'Add new word' sceen will be dispalyed with the clicked word as the word to translate. Then the user can provide missing details manually or use AI option.,
I personally use this feature mainly while reading a book. It is more convenient just to record a list of new words instead of having to type them in.</p>

<img src="/Foreign Words Dictionary/Images/TranscriptionsScreen.jpg" width="200">
<br>

<img src="/Foreign Words Dictionary/Images/NewWordInfo.jpg" width="200">
<br>

