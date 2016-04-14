# Guide

## Javascript API

There's a simple `starRatingService` that can be used in your app code.

```js
// On Server or Client
import { Tracker } from 'meteor/tracker';
import { starRatingService } from 'meteor/arkham:stars-rating-ui';

Tracker.autorun(function () {
    // Get all ratings for a specific id
    starRatingService.getRatings('someId');
    // Get average rating of an id
    starRatingService.getAverageRating('someId');
    // Get rating of currenty logged in user
    starRatingService.getRatingForCurrentUser('someId');
    // Get rating of specific user by id
    starRatingService.getRating('someUserId', 'someId');
});

// Rate as your currently logged in user
starRatingService.rate('someId', 4);
```