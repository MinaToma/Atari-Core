# Atari-Core
Game Engine to facilitate designing java games.

## How to use?
- [Helper Class](https://github.com/MinaToma/Atari-Core/blob/master/src/atariCore/Helper.java)
  - call `Helper.Load()` function to load all images from the _res_ folder.
  - you can change any variable value to suit if needed.
  
- [Splash Class](https://github.com/MinaToma/Atari-Core/blob/master/src/atariCore/Splash.java)
  - provide frame title and font file path.
    ```java 
        public Splash(String title, String fontFile) {
          //class constuctor
        }
    ```
  - set buttons' actions
  
- [Game Class](https://github.com/MinaToma/Atari-Core/blob/master/src/atariCore/Game.java)
  - initialise Keyboard & Mouse Actions.
  - implement required functions.
  - provide frame title.
    ```java 
        public Game(String title) {
          //class constuctor
        }
    ```
- [BaseObject Class](https://github.com/MinaToma/Atari-Core/blob/master/src/atariCore/BaseObject.java)
  - all game objects should inherit this class.
   - provide position, image and object behavior.
      ```java 
          public BaseObject(float x, float y, Image image, float velX, float velY) {
            //class constuctor
          }    
          protected abstract void tick();    
          protected abstract void render(Graphics g);
      ```
- [Handler Class](https://github.com/MinaToma/Atari-Core/blob/master/src/atariCore/Handler.java)
  - all objects should be inserted in this list 
    ```java
    private static CopyOnWriteArrayList<CopyOnWriteArrayList<BaseObject>> object = new CopyOnWriteArrayList<>();
    ```
  - add all game object lists of type _CopyOnWriteArrayList\<BaseObject\>_ <br> 
  using
    ```java
      public void addHandler(CopyOnWriteArrayList<BaseObject> list)
    ```

- [SelectPlayer Class](https://github.com/MinaToma/Atari-Core/blob/master/src/atariCore/SelectPlayer.java)
  - implement to set buttons' actions 
    ```java
        protected abstract void setActions();
    ```

## Developers

| Name                     | Account                                                      |
| ------------------------ | ------------------------------------------------------------ |
| Mahmoud Medhat Mehisen   | [@MahmoudMehisen](https://github.com/MahmoudMehisen)         |
| Mariam Mostafa           | [@MariamMostafa27](https://github.com/MariamMostafa27)       |
| Mina Toma                | [@MinaToma](https://github.com/MinaToma)                     |
| Youssef Sobhy            | [@YoussefSobhy](https://github.com/youssefsobhy)             |
| Ziad Abd Elrahman        | [@ZiadAbdElrahman](https://github.com/ZiadAbdElrahman)       |


### Notes
For further information read atariCore's [javadoc](https://github.com/MinaToma/Atari-Core/tree/master/res/Javadoc) and to see the core in action checkout [AI-Atari](https://github.com/MinaToma/AI-Atari)
