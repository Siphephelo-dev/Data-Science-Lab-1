# Reflection – Movie Recommendation System

## Which method worked better?  
- **Collaborative Filtering** worked best when there were enough overlapping ratings between users. It was able to recommend movies that similar users had already enjoyed.  
- **Content-Based Filtering** was more reliable when users had very few ratings. Since it uses the movie genres, it could still generate meaningful recommendations without needing many user-to-user comparisons.  
- Overall, **Content-Based Filtering** produced more consistent results on this dataset, while Collaborative Filtering would perform better with a larger, denser dataset containing more user ratings.  

---

## Challenges Faced  
1. **Missing Data**: Many users had very few ratings, which limited Collaborative Filtering’s ability to find strong similarities.  
2. **Cold Start Problem**:  
   - New users with no ratings could not get recommendations from Collaborative Filtering.  
   - New movies with no ratings could not be recommended either.  
   - Content-Based Filtering helped address this, but only if genre information was present.  
3. **Sparse Matrix**: The user–item rating matrix had many empty cells. Filling them with zeros allowed similarity calculations but reduced accuracy in some cases.  

---

## Final Thoughts  
Both methods have their strengths:  
- Collaborative Filtering benefits from more data and performs well when users share similar tastes.  
- Content-Based Filtering is more resilient to sparse data and new users, as long as item attributes (like genres) are available.  

For this project, **Content-Based Filtering worked better overall**, but combining both approaches (a hybrid system) could lead to the most effective recommendations.  
