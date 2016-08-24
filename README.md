# YII2 Generate image url form anywhere

> Use the below function to generate image url from anywhere in Yii2 framework
```
    /**
     * Generate Profile Image from usermname string
     * @param $imageName is the image name saved in the database
     * @param $type is the directory name save in param.php file
     * @return string Complete base url of an image
     */
    private static function generateImagePath($imageName, $type)
    {
        if(is_null($imageName))
        {
            return null;
        }
        $varImageUrl = Url::base(true).Yii::$app->params[$type].$imageName;
        return $varImageUrl;
    }
```
