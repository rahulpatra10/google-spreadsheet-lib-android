This Library helps to develop Android applications which can access Google SpreadSheets. Though Google has mentioned that GData API supports SpreadSheet API on Android, but this is not the case. There are multiple forums pointing this problem without any solution [Problem#1](http://code.google.com/p/android/issues/detail?id=1865) [Problem#2](http://groups.google.com/group/android-developers/browse_thread/thread/1e261f25c828e39f?pli=1).

It has been developed in Java with no platform dependency, so can be used in any Java based platform (Desktop, Android, J2ME and RIM).

Following are the supported features-<br><br>
- Supports both <a href='http://code.google.com/apis/spreadsheets/data/3.0/developers_guide.html#ListingSpreadsheets'>List</a> and <a href='http://code.google.com/apis/spreadsheets/data/3.0/developers_guide.html#TableFeeds'>Table</a> feed <br>
- Create/Delete SpreadSheet <br>
- Create/Delete WorkSheet <br>
- Insert/Update/Delete Worksheet data <br>
- Conditional data retrieval (Structured Query support)<br>
- Share SpreadSheet with other users (Gmails IDs) <br>
- 2 types of Authentications. <i>Basic Authenticator and Android Authenticator</i>. Basic Auth is suitable for non-Android applications where application need to prompt users for Gmail ID and Password. Whereas Android Auth uses Android's Account Manager concept and requires the relevant Gmail account should be registered under <i>"Settings | Accounts and Synch"</i>.<br>
<br>
The <b>sample Android client application</b> includes <i>AndroidAuthenticator.java</i> which you can re-use.<br>
<br>
<b>Kindly note:</b><br>
- This library doesn't support any persistent caching facility and if user plan for any caching, they need to develop separate logic.<br>
<br>
- Prior to use the Sample Android application, make sure you have registered a valid Gmail Account under <i>"Settings | Accounts and Synch"</i>.<br>
<br>
- <i>Android emulator strips out few XML feed prefix</i> and thus need to add following line at the very beginning if you want to use this library in emulator-<br>
<pre><code>if("sdk".equals(Build.PRODUCT) || "google_sdk".equals(Build.PRODUCT))<br>
    ParseFeed.doCustomizationForSDK(); <br>
</code></pre>

Share your feedback, queries, comments on <a href='http://prasanta-paul.blogspot.com/2010/12/google-spreadsheet-library-for-android.html'>my blog</a>, I'm listening :-)<br>
<br>
<b>Donation:</b> For making donation please visit <a href='http://prasanta-paul.blogspot.com/2010/12/google-spreadsheet-library-for-android.html'>my blog</a>