
***Somstem Anonymous Repository***
>📋 Somstem Overall Architecture:
<img src="assets/design.jpg" width=700>

## Usage 

>📋 Click [somstem](https://github.com/AMoffsom/Som_stem/releases/tag/V1.0) and download the somstem.zip file.
1. Download the project from the above provided link.
2. Extract the ZIP file to retrieve the Somstem folder. You may see a path like somstem/Somstem. Make sure to use the correct directory when accessing the files.
3. Place it in your project directory or any location of your choice, and then follow the steps outlined below.

## Requirements

>📋 First, install the stemmer, then the other requirements:
```
pip install directory/somstem/dist/somstem-0.1.0-py3-none-any.whl   
```
- example in my case:   pip install D:/pos-tagger/somstem/dist/somstem-0.1.0-py3-none-any.whl

```
transformers                
torch                        
datasets                     
sentencepiece
scikit-learn                            
```
- In a future version, we will remove the scikit-learn package.
  
>📋 We met an error in a TensorFlow installed machine and solved installing:
```
pip install protobuf
```



## Sample Code

```
from  somstem.mt5_last import HybridStemmer
if __name__ == "__main__":

       hybrid_stemmer = HybridStemmer()
       while True:
        word_to_stem = input("Enter a word to stem or type 'quit' to exit: ")
        if word_to_stem.lower() == "quit":
            print("Exiting the program.")
            break
        stemmed_word = hybrid_stemmer.stem(word_to_stem)
        print(f"Original word: {word_to_stem}")
        print(f"Stemmed word: {stemmed_word}")
```

>📋 Output:

```
Enter a word to stem or type 'quit' to exit: xarunta
Original word: xarunta
Stemmed word: xarun
Enter a word to stem or type 'quit' to exit: 
```
