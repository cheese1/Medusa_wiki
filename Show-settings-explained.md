

-------------------

[ [Add Show button] ](https://github.com/pymedusa/Medusa/wiki/Show-settings-explained#add-show-button) [ [Shows overview and buttons explained] ](https://github.com/pymedusa/Medusa/wiki/Show-settings-explained#shows-overview-and-buttons-explained) [ [Shows Edit Button] ](https://github.com/pymedusa/Medusa/wiki/Show-settings-explained#shows-edit-button)   

---------------------


##Add Show button

* This button allows you to add a new or existing shows. 

![show-overview](https://cloud.githubusercontent.com/assets/7928052/13013808/699a06d6-d1b1-11e5-95e8-5969fa39a6c0.png)

#### Adding a new Show

![add-show-2](https://cloud.githubusercontent.com/assets/7928052/13013853/90d9687c-d1b1-11e5-9715-fa896f335fe3.png)

*Step 1*  

Once you clicked on the new show button you will be asked to enter the name of the show you like to search/add. In this example "game of thrones". Further you can set a language that you want to use for the show, like descriptions etc. And last the preferred indexer where Medusa should search. When you are ready push search. Now any results found will be showed in the lower part of the screen. Select the show you want end click `next`.  (Alternatively you can click on the `add` button, however this will skip the customization settings.!)  


![add-show-4](https://cloud.githubusercontent.com/assets/7928052/13013855/90fb70fc-d1b1-11e5-9a9e-f1d977a578d9.png)

*Step 2*  

Now that we have selected the show we are actually going to add it. 
In case you have not set a Root folder yet, (the folder where you want to place your shows) use the `new` button to add one. And again press `next` 

![add-show-5](https://cloud.githubusercontent.com/assets/7928052/13013856/90fe025e-d1b1-11e5-89c2-a35f4dad127a.png)

*Step 3*  

Here you have the possibility to customize the shows settings.   

 * `subtitles`  
Should subtitles be enabled for this show. Allows Medusa to search for subtitles.  
 * `Status for previously aired episodes`  
What status should be set for episodes that have already been aired?  
 * `Status for all future aired episodes`  
What status should be set for episodes that have NOT yet aired? (Set Wanted or no newly aired episodes will be downloaded!)
 * `Flatten Folders`  
 * `Anime`  
Is this an Anime show and should Medusa use Anime functions?
 * `Scene Numbering`  
Should Medusa use [Scene Numbering](https://github.com/pymedusa/Medusa/wiki/Scene-exceptions-and-numbering#what-is-scene-numbering)?  
 * `Preferred quality of episodes to be downloaded`  
What [quality](https://github.com/pymedusa/Medusa/wiki/Quality-Settings) should Medusa use?  
 * `Save Defaults`  
This allows the settings you have selected to be saved as defaults, So you dont have to manually select them next time adding a show.  
Now that you have setup all settings press the `add` button.  


#### Add popular IMDB shows  

![imdb](https://cloud.githubusercontent.com/assets/7928052/13013857/90ff50fa-d1b1-11e5-828c-80a0837dd1e2.png)

This nice feature gives you an overview of the current popular/trending TV shows on [IMDB](http://www.imdb.com/) and lets you add them. It uses the IMDB MOVIEmeter Rating system, that ensures reliably results. Give it a try, and learn the shows you should consider adding. Shows that already are in your list will be hidden.    

#### Add popular Trakt shows  

![trakt](https://cloud.githubusercontent.com/assets/7928052/13013858/9101c5ec-d1b1-11e5-815c-8c108fb2415f.png)

Similar to the IMDB popular shows option, here you can add Trending shows from [Trakt](https://trakt.tv/).  


#### Adding an existing show 

* Medusa also has the ability to add existing shows. Unlike newly added shows a existing show has already a folder with the episodes and/or meta data present. 

![add-existing](https://cloud.githubusercontent.com/assets/7928052/13013854/90ecd20e-d1b1-11e5-9066-3092293c7e99.png)

Adding an existing show basically works the same as a new show. The main difference is that you need to select the folder where the show is located. Set/add the root folder where the show(s) are located and Medusa will give an overview of all the (not yet used) folders and allow you to set an indexer to search.  You can add multiple shows at once or just one singe show. 

In case you are using meta-data/nfo files and have the tvshow.nfo file in a series folder, the adding process will go automatically.  


![add-show-8](https://cloud.githubusercontent.com/assets/7928052/13013859/9101cace-d1b1-11e5-9197-7a4fe11ade15.png)

Just as adding a new show you can set custom settings for the show(s). If you like to set every shows manually than enable the option `prompt me to set settings for each show`  : 


 * `subtitles`  
Should subtitles be enabled for this show. Allows Medusa to search for subtitles.  
 * `Status for previously aired episodes`  
What status should be set for episodes that have already been aired?  
 * `Status for all future aired episodes`  
What status should be set for episodes that have NOT yet aired? (Set Wanted or no newly aired episodes will be downloaded!)
 * `Flatten Folders`  
 * `Anime`  
Is this an Anime show and should Medusa use Anime functions?
 * `Scene Numbering`  
Should Medusa use [Scene Numbering](https://github.com/pymedusa/Medusa/wiki/Scene-exceptions-and-numbering#what-is-scene-numbering)?  
 * `Preferred quality of episodes to be downloaded`  
What [quality](https://github.com/pymedusa/Medusa/wiki/Quality-Settings) should Medusa use?  
 * `Save Defaults`  
This allows the settings you have selected to be saved as defaults, So you dont have to manually select them next time adding a show.  
Now that you have setup all settings press the `add` button.  
   

##Shows overview and buttons explained  

![show-overview](https://cloud.githubusercontent.com/assets/7928052/13013866/9a6978a0-d1b1-11e5-9db3-7949c77f9ce5.png)

1 `Edit`  
Opens the edit section of the show. Here you can specify your settings for this show.  
2 `Pause`  
This will Pause/Resume your show. If paused no newly aired episodes will be downloaded.  
3 `Remove`  
Lets you remove the show from Medusa. When pushed you will get an pop-up screen with the question to remove the show with or without he file/folder.  
4 `Re-Scan`  
Rescans all the files in your shows folder. Episodes,subtitles and metadata. etc.  
5 `Force-Full Update`  
Forces a full update of your shows data from the indexer. Replaces the old data in the database. Can be helpful in case you have problems with air dates, metadata etc.  
6 `Preview Rename`  
Opens the Preview Rename page. It allows you to see how the files will look like after the rename, if you have setup renaming in post-processing.  
7 `Download Subtitles`  
Starts an automatic search for missing subtitles for the show.  
8 `Change Show:`  
This settling lets you quickly navigate between shows without returning to the main page.  
9 `Display Specials`  
Lets you hide specials from the page.  
9 `Seasons`  
Lets you quick jump to the selected season.  
10 `Summery`  
Summery of the show. This includes  : Name, IMDB score, production country/year, links to indexer/IMDB/XEM, genre, Quality, airtime, Show Status, default EP Status, file path, Scene Name, Size.  
11 `Setting overview`  
Gives a quick overview of the most important settings that are in use for the show.  
12 `Change selected episodes to:`  
Lets you set individual episodes to your preferred status.  
13 `Status check-boxes`  
Lets you select what episodes should be showed with what status.   
14 `select columns` 
This lets you customize the columns of the seasons. You can add the seize columns or the filename columns etc.  The columns that can be set are:   
`NFO`             Shows if a [*.nfo](http://kodi.wiki/view/NFO_files/tvepisodes) is present for the episode in the folder.  
`TBN`             Shows if there are covers, banner, posters, thumbnails, or fanart in the folder.  
`Episode`         Shows the episode number supplied by the indexer.  
`Absolute`        Shows the Absolute supplied by the indexer.  
`Scene`           Adds a field to manually enter a scene number.  
`Scene Absolute`  Adds a field to manually enter a scene absolute number.  
`Name`            Shows the episode name supplied by the indexer.  
`File name`       Shows the file name of the episode.  
`Seize`           Shows the seize of the episode file.  
`Airdate`         Shows the air-date of the episode.  
`Download`  
`Subtitles`       Shows the subtitles that are downloaded with a small flag.  
`Status`          Shows the status of the episode. (wanted,skipped, downloaded HDTV etc.)  
`Search`          By clicking on the search glass you can manually search for an episode.  


##Shows Edit Button  

![Main Settings](https://cloud.githubusercontent.com/assets/7928052/13013867/9cd2c2fe-d1b1-11e5-8929-596558a0105c.png)


#### Main Settings

* `Show Location:`  
Lets you set the location of the shows folder.  
* `Preferred Quality:`  
Lets you set the quality of the file that Medusa should download. See [Quality Settings](https://github.com/pymedusa/Medusa/wiki/Quality-Settings) for more info.  
`Default Episode Status:`  
Lets you set the Default Episode Status. Needs to be set to WANTED if you want new shows to be downloaded.! See [Default Episode Status](https://github.com/pymedusa/Medusa/wiki/FAQ%27s-and-Fixes#newly-aired-shows-are-not-downloading-and-set-to-skippedignored) for more info.  
* `Info Language:`  
Lets you set the default language for the show. Info, descriptions etc. Note, not subtitles.!  
* `Subtitles:`  Enable or disable the automatic download of subtitles for this show.  
* `Paused:`  Lets you pause the show. Prevents shows from being downloaded.  

![Format](https://cloud.githubusercontent.com/assets/7928052/13013967/f3afb3fc-d1b1-11e5-845b-e15894ef8e00.png)

* `Air by date:`  Select if the shows contains the air-date instead of the normal S01E01 format in the title.   
* `Anime:`  Select if the show only contains an episode number instead of the normal S01E01 format in the title.  
* `Sports:`  ?  
* `Seasons folders:` Sort episodes in seasonal folders. Disable if you like all episodes in one folder.  
* `Scene Numbering:`  Enable or disable Scene Numbering. See [Scene Numbering](https://github.com/pymedusa/Medusa/wiki/Scene-exceptions-and-numbering#what-is-scene-numbering) for more info.  
* `DVD Order:`  ?  

![Advanced](https://cloud.githubusercontent.com/assets/7928052/13013968/f3d5ba48-d1b1-11e5-901a-5f033ccefdea.png)

* `Scene Exception:`  
Lets you set and remove Scene Exceptions. See [Scene exceptions and numbering](https://github.com/pymedusa/Medusa/wiki/Scene-exceptions-and-numbering) for more info.  
* `Archive on first match:`  check this to have the episode archived after the first best match is found from your archive quality list.  
* `Ignored Words:`  All releases containing those words will be skipped.! Use with caution.!  Separate words with a comma, e.g. "word1,word2,word3"  
* `Required Words:`  All releases NOT containing those words will be skipped.! Use with caution.! Separate words with a comma, e.g. "word1,word2,word3"  
  