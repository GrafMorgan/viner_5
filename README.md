1. Создаём новый проект
2. Добавляем VideoView
![image](https://user-images.githubusercontent.com/38504787/145618749-dfada797-5e82-4585-b341-f49f45f83381.png)
3. Создадим папку ресурсов "raw" в папке "res" и закинeм в неё видео
![image](https://user-images.githubusercontent.com/38504787/145618840-5184b48f-c778-425c-9818-909be6b6df6b.png)
4. Пишeм код:
~~~ Java
VideoView videoView =(VideoView)findViewById(R.id.videoView);
        MediaController mediaController= new MediaController(this);
        mediaController.setAnchorView(videoView);
        Uri uri = Uri.parse("android.resource://" + getPackageName() + "/" + R.raw.adventuretimetheme);
        videoView.setMediaController(mediaController);
        videoView.setVideoURI(uri);
        videoView.requestFocus();
        videoView.start();
~~~
5. Проверяем:
![image](https://user-images.githubusercontent.com/38504787/145619248-2be60440-3f1b-4657-a382-1cabea6cbd32.png)
