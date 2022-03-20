# Hi! Welcome To My First Website 🥳

Here is a meme I created using the [{Magick}](https://cran.r-project.org/web/packages/magick/vignettes/intro.html) package from **R**.

![](meme.png)

*The code that was used to create this meme:*

* `library(magick)`

* `happy_guy <- image_read("https://pbs.twimg.com/media/FMrwNcdX0AMAzOG.jpg") %>% 
  image_scale(345)`
  
* `disappointed_guy <- image_read("https://www.meme-arsenal.com/memes/09c215c9219d02c6c80a0fb639d75317.jpg") %>%
  image_scale(340)`

* `text1 <-image_blank(width = 400, height = 280, color = "#000000") %>%
  image_annotate(text = "Changes language on\nphone for fun", color = "#ffffff", size = 35, font = "sans", gravity = "center")`

* `text2 <-image_blank(width = 400, height = 280, color = "#000000") %>%
  image_annotate(text = "Can't find language\nsetting anymore", color = "#ffffff", size = 35, font = "sans", gravity = "center")`

* `first_row <- c(text1, happy_guy) %>%
  image_append()`

* `second_row <- c(text2, disappointed_guy) %>%
  image_append()`

* `final_vector <- c(first_row, second_row)`

* `final_meme = image_append(final_vector, stack = TRUE)`

* `image_write(final_meme, "final_meme.png")`

## Motivation/Inspiration For This Meme 🤔

1. I searched through many memes on Google and found one that I thought was funny 🤣
2. I copied the joke from the meme, but replaced the photos with ones I had also found on Google!
