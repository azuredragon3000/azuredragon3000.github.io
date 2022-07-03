#different between listview and recycleview.  
  
The main difference between ListView and GridView is how it lays out its child. With ListView you are laying your children one by one either vertically or horizontally only. With GridView, its a combination of both. It lays its children horizontally first.  
  
#different between listview and GridView.  

RecyclerView was created as a ListView improvement, so yes, you can create an attached list with ListView control, but using RecyclerView is easier as it:  
  
Reuses cells while scrolling up/down - this is possible with implementing View Holder in the ListView adapter, but it was an optional thing, while in the RecycleView it's the default way of writing adapter.  
  
Decouples list from its container - so you can put list items easily at run time in the different containers (linearLayout, gridLayout) with setting LayoutManager.  
  
Example:  
  
    mRecyclerView = (RecyclerView) findViewById(R.id.my_recycler_view);
    mRecyclerView.setLayoutManager(new LinearLayoutManager(this));
    //or
    mRecyclerView.setLayoutManager(new GridLayoutManager(this, 2));
    Animates common list actions - Animations are decoupled and delegated to ItemAnimator.
    There is more about RecyclerView, but I think these points are the main ones.
  
So, to conclude, RecyclerView is a more flexible control for handling "list data" that follows patterns of delegation of concerns and leaves for itself only one task - recycling items.  
  
#implement GridView and Listview.  
#batch file basic.  
#gradle script basic.  
#procese excel poi java.  
#process strijg java pattern.  
#create folder and list folder in java.  
#read and write file basic in java.  
#handlel databasee
