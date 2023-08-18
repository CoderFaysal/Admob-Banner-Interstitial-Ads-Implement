# Ads Implement

```
implementation 'com.google.android.gms:play-services-ads:22.2.0'
```

# Manifest

```
<uses-permission android:name="com.google.android.gms.permission.AD_ID"/>
```

```
<!-- Sample AdMob app ID: ca-app-pub-3940256099942544~3347511713 -->
<meta-data
        android:name="com.google.android.gms.ads.APPLICATION_ID"
        android:value="ca-app-pub-3940256099942544~3347511713"/>
```



# Banner Ads


## XML

```
<LinearLayout
        android:id="@+id/banner"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_alignParentTop="true"
        android:layout_marginBottom="5dp"
        android:orientation="vertical"
        android:layout_marginTop="5dp"
        />
```

## JAVA onCreate

```
Admob.setBanner(view.findViewById(R.id.banner), getContext());
```


# Interstitial Ads
## JAVA onCreate 

```
Admob.loadInt(MainActivity.this);
```


## Button Click

```

new Admob(new OnDismiss() {
  @Override
  public void onDismiss() {

    startActivity(new Intent(getActivity(), VideoPlayer.class));

  }
}).ShowInterstitial(getActivity(), true);

```
