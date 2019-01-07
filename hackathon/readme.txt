Explanation of hackathon project :

1) **main_emojis.ipynb**
  - Connect to weibo DB
  - Select all the status and the related location
  - Create a dataframe with all status that include emojis (contained in [ ] ) and create a csv ( **emoji_status.csv** )
  - With this csv open, count the occurence of each emoji and create a csv with it ( **emoji_use.csv** )
  
2) **emoji_status_rated.csv**
  - For each emoji, we create 6 scores related to the 6 emotions, from -5 to 5 and we translate it 
  
3) **score_id.ipynb**
  - Connect to weibo DB
  - Select all the status and the related location
  - Create a dataframe with all status that include emojis (contained in [ ] )
  - For each status, count the occurences of emojis in it
  - Using **emoji_status_rated.csv**, for each status, we analyze the emojis in it and give a score for emotions, in the shape {location_id, (a,b,c,d,e,f,g)}
  - We save the results in **loc_feeling_rating.csv**
  
4) **selection.ipynb**
  - With **loc_feeling_rating.csv**, we give a choice of what the user want to feel 
  - We extract the top result of the feeling, removing 1% of the top results to avoid huge scores
  - We take 10 out of the 20 top results 
  - We make a request to get the detailed information about those results
  
  
 Extras :
  - Pearl tower files are  targetted test on pearl tower status
