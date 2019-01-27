# L'AudioManager

## But du TD
Dans ton projet MediaPlayer, lorsqu'une autre application demande à prendre la main sur l'audio, ton application ne se *mute* pas et ça peut devenir très désagréable.
Android n'arbitre pas l'audio au sein des applications tierces et pour ne pas être intrusif, il faut s'enregistrer à l'AudioManager pour savoir si oui ou non on a le droit d'émettre un son (musique, bip, ...).

* Tu vas devoir intégrer l'audioManager à ton projet MediaPlayer.
* Tu peux reprendre ton MediaPlayer ou alors tu peux récupérer une version [ici](https://github.com/WildCodeSchool/dojo-android-audio-player).

## Etapes
### Demander à l'audioManager d'avoir le focus audio
* Tu vas demander à l'[AudioManager](https://developer.android.com/reference/android/media/AudioManager) l'autorisation d'écouter la chanson lorsque tu cliqueras sur le bouton PLAY.
* S'il accepte, tu peux lancer la lecture.

### S'enregistrer à l'AudioManager afin d'être informé lorsque l'état du focus change
* Maintenant, tu vas t'enregistrer avec un listener à l'AudioManager pour mettre en pause la chanson lorsqu'une autre application demandera le focus sur l'audio.

### Libérer le focus audio à la fermeture de l'application
* Finalement, à la fermeture de l'application, libère proprement l'AudioManager.

## Documentation
* [AudioManager](https://developer.android.com/reference/android/media/AudioManager)
* [audio-focus](https://developer.android.com/guide/topics/media-apps/audio-focus)
