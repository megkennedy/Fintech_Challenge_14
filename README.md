# Fintech_Challenge_14
UW Fintech Bootcamp Challenge 14


### Model 1

Model one has a DateOffset of 3 months

SMA short =4

![Model 1 plot](https://user-images.githubusercontent.com/88640228/143805802-299fe8cf-ea09-4b6d-8536-4a7c7a1688e1.png)


### Model 2

Model two has a DateOffset of 6 months

SMA short=4

![Model 2 plot](https://user-images.githubusercontent.com/88640228/143805836-4d44d80c-6410-4be9-bb19-29a075937803.png)


### Model 3

Model three has a DateOffset of 3 months

SMA short=20

![Model 3 plot](https://user-images.githubusercontent.com/88640228/143805849-62ea537d-6ecb-42b7-8c55-7968ad265dbf.png)

### Model 4

Model four has a DateOffset of 4 months

SMA short =4

![Model 4 plot](https://user-images.githubusercontent.com/88640228/143805871-bbd4a386-8421-4469-b1ce-eb4455369b1b.png)


### Model Manipulation Analysis
When adjusting the SMA short and the SMA long (not pictured) it made the model's predictions less accurate. Therefore, further adjustments were made to the DateOffset to see if that would increase the accuracy of the predictions. While six month offset showed fair accuracy when comparing the actual returns line to the strategy returns, when the DateOffset was reset to 8 (not pictured) the resulting graph was less accurate. The final model chosen was a DateOffset of four months which once again shows the two lines running close together. 
