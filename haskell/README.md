## Functor

```haskell
class Functor f where
  fmap :: (a -> b) -> f a -> f b
```

## Applicative Functor

```haskell
class (Functor f) => Applicative f where
  pure :: a -> f a
  (<*>) :: f (a -> b) -> f a -> f b
```

#### Maybe
```haskell
instance Applicative Maybe where
  pure = Just
  Nothing <*> _ = Nothing
  (Just f) <*> something = fmap f something
```

#### List
```haskell
instance Applicative [] where
  pure x = [x]
  fs <*> xs = [f x | f <- fs, x <- xs]
```

## Monad
```haskell
class Monad m where
  return :: a -> m a
  
  (>>=) :: m a -> (a -> m b) -> m b
  
  (>>) :: m a -> m b -> m b
  x >> y = x >>= \_ -> y
  
  fail :: String -> m a
  fail msg = error msg
```
