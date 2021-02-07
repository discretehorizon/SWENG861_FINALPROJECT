## Doppler Design Document

### Table of Contents
1. [Background](#background)
1. [Objectives](#objectives)
1. [Use Case](#usecase)
    1. [Use Case 1: Searching for an Artist](#usecase1)
    1. [Use Case 2: Searching for a Song](#usecase2)
1. [Requirements](#requirements)
1. [Appendix A: Requirements Implementation Plan](#requirementsimp)

<a name="background"></a>
### 1. Background

In 2019, the US music industry's revenue [surpassed $11.9 billion](https://www.billboard.com/articles/business/8551881/riaa-music-industry-2019-revenue-streaming-vinyl-digital-physical/). A considerable contribution to this growth is streaming music services. These services rely on and employ a variety of APIs to meet customer demands. The class project for SWENG 861 is to explore REST APIs by building a client that consumes a service. Due to the impact that music has on the economy and the author of this paper's affinity toward music, a music research tool called Doppler is under design. The name originates from physics where [The Doppler Effect](https://en.wikipedia.org/wiki/Doppler_effect) describes how frequency changes based on the relative motion of a wave source and an observer. Just as the listener's perception of sound can be changed based on their physical location in space, a similar effect occurs when the same song might sound different to the same person, depending on their social location.  At any one time, a person's personality, culture, attitude, and personal preferences may change due to their circumstances and experiences.


<a name="objectives"></a>
### 2. Objectives

<a name="usecase"></a>
### 3. Use Case

The system addresses two use cases: (1) the case where a user wants to research an artist and (2) the case where the user wants to research a particular song.

<a name="usecase1"></a>
#### 3.1 Use Case 1: Searching for an Artist

The user has a particular artist in mind.  First, the user opens the app by double-clicking it.  Then they are presented with the search form.  On the search form, the search type "artist" is the default selection, and does not require modification by the user.  Then the user inputs the name of the artist in the search field. The app then displays a list of artists that match the search criteria.  The user can then select the intended artist from the list.  The app then displays information about the artist.  A search form is located on each page to allow a user to initiate a new search at any time.

<a name="usecase2"></a>
#### 3.2 Use Case 2: Searching for a Song

The user has a particular song in mind.  First, the user opens the app by double-clicking it.  Then they are presented with the search form.  On the search form, the user must change the search type selection to "song."  Then the user inputs the name of the song in the search field. The app then displays a list of songs that match the search criteria.  The user can then select the intended song from the list.  The app then displays information about the song.  A search form is located on each page to allow a user to initiate a new search at any time.

<a name="requirements"></a>
### 4. Requirements


* Req1 - Implement a web service client
    * Req1.1 - Use language of choice, language must work with selected client-side technologies
	* Req1.2 - Use technologies capable of REST calls to external service API
	* Req1.3 - Use REST api that enables access to music 
	information
	* Req1.4 - Multiple REST api calls should be possible
	* Req1.5 - Code should be well documented
* Req2 - End-user can inquire about a song or a singer
	* Req2.1 - A user may search by song title
	* Req2.2 - A user may search by artist name
* Req3 - Program will output information regarding the input
	* Req3.1 - Output may include: singer name, composer name, date of release, lyrics, song title etc.
* Req4 - Provide a command line or GUI interface
    * Req4.1 - Interface must provide input validation
    * Req4.2 - Interface will allow user to select type of search
    * Req4.3 - GUI is preferred
    * Req4.4 - Interface must not be One-and-Done

<a name="requirementsimp"></a>
### Appendix A: Requirements Implementation Plan

#### Req1 - Implement a web service client
Implementation | Req1.1 | Req1.2 | Req1.3 | Req1.4 | Req1.5
-- | -- | -- | -- | -- | -- |
The application will be written in Javascript.|<font size="20px">x</font>|<font size="20px">x</font>|
Electron.js is the application framework.||<font size="20px">x</font>
The Musixmatch API will be used <https://developer.musixmatch.com/>|||<font size="20px">x</font>|<font size="20px">x</font>
Every function and section of developed code will be documented.|||||<font size="20px">x</font>
 
#### Req2 - End-user can inquire about a song or a singer
Implementation | Req2.1 | Req2.2 
-- | -- | -- 
A user will be able to search by song title.  A list of song's will be returned to the user allowing them to select the one they were looking for.|<font size="20px">x</font>
A user will be able to search by artist name.  A list of artists will be returned to user allowing them to select the artist they wanted to see.||<font size="20px">x</font>

#### Req3 - Program will output information regarding the input
Implementation | Req3.1 
-- | -- 
The following will be displayed as appropriate to the request: artist name, date of release, lyrics, and song title.|<font size="20px">x</font>

#### Req4 - Provide a command line or GUI interface
Implementation | Req4.1 | Req4.2 | Req4.3 | Req4.4 
-- | -- | -- | -- | -- 
HTML will be used for high level organization of interface elements.|||<font size="20px">x</font>
CSS will be used to provide styles.|||<font size="20px">x</font>
Vue.js will be used to bind data to interface.|||<font size="20px">x</font>|<font size="20px">x</font>
Bootstrap will be the component library.||<font size="20px">x</font>|<font size="20px">x</font>
The search field will need more than three characters to proceed.|<font size="20px">x</font>
The search field is a required field.|<font size="20px">x</font>
Searches must start with a letter.|<font size="20px">x</font>
User input will be escaped before transmitting.|<font size="20px">x</font>
Popper.js will be used to provide user feedback on input validation.|<font size="20px">x</font>
