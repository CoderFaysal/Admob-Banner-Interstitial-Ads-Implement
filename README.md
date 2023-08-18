# Main Activity onCreate 

```
Admob.loadInt(MainActivity.this);
```


# Button Click

```

new Admob(new OnDismiss() {
  @Override
  public void onDismiss() {

    startActivity(new Intent(getActivity(), VideoPlayer.class));

  }
}).ShowInterstitial(getActivity(), true);

```
