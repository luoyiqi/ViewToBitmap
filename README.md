### ViewToBitmap

An Android library that makes it very easy and very quick to save any View or ViewGroup as an image to the gallery.  
Perfect for photofiltre, quotes and drawing apps! Feel free to try the .apk sample.

Currently used in:
- [Quote Creator] (https://play.google.com/store/apps/details?id=org.m.muddzboy.QuoteCreator&hl=da) with +90.000 downloads!
- [Shoppist] (https://play.google.com/store/apps/details?id=com.muddii.shopping_list&hl=da)

*Feel free to contact me if you want your app to be included here*

<a href="https://github.com/Muddz/ViewToBitmap/raw/master/ViewToBitmap-sample.apk">Download the sample .apk: </a>

### Features

- The library saves in an ```AsyncTask```
- Options to save Bitmaps in the formats: ```.JPG```  ```.PNG ``` ```.nomedia```
- Option to put quality variable for ```JPG``` formats
- Optional listener that gives you a boolean value and String path when/if the image is saved
- Set the name of the  ```Bitmap ``` files and folders. They have by default a timestamp as name for each save  
- Support from API 16+

----

### Example of simple usage

```java
        
    ViewToBitmap image = new ViewToBitmap(drawingBoard);
    image.setOnBitmapSaveListener(this);
    image.saveToGallery();
        
   
   //With optinal listener
    @Override
    public void onBitmapSaved(final boolean isSaved, final String path) {
        if (isSaved) {
            Toast.makeText(this, "Bitmap Saved at; " + path, Toast.LENGTH_SHORT).show();
        }
    }  
    
```
    
    
### Installation

Add the depedency in your build.gradle. The library is distributed via jCenter

```groovy
dependencies {
    compile 'com.muddzdev:viewtobitmap:1.0.7'    
}
```
 ----

### License

    Copyright 2017 Muddii Walid (Muddz)

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
