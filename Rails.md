# Railsコーディング規約

## 行数
- 一行を最大79文字までに抑える。

## インデント
- インデントの幅は2つとする。

良い例:
```ruby
if a < 0
  return true
else
  return false
end
```

悪い例:
```ruby
if a < 0
    return true
else
    return false
end
```

## 空行
- 複数のクラス、メソッドを定義する際は必ず空行を開けること。 

良い例:
```ruby
class Foo
  def self.hoge_1()
    ...
  end

  def hoge_2()
    ...
  end
end

class Bar
  ...
end
```

悪い例:
```ruby
class Foo
  def self.hoge_1()
    ...
  end
  def self.hoge_2()
    ...
  end
end
class Bar
  ...
end
```

## メソッドの定義
- メソッドの定義の際、引数の有無に関わらず括弧をつける。  

良い例:
```ruby
def str(x, y)
  ...
end

def str()
  ...
end
```

悪い例:
```ruby
def str
  ...
end
```

## クラスメソッドの定義
- クラスメソッドを定義する場合は必ず先頭にselfを付ける。  

良い例:
```ruby
class Hoge
  def self.hoge
    ...
  end
end
```

悪い例:
```ruby
class Hoge
  def Hoge.hoge
    ...
  end
end
```

## メソッドの呼び出し方法
- メソッドを呼び出す際は引数の有無に関わらず、必ず括弧をつけること。

良い例:
```ruby
foo(x, y)
Foo.foo(x, y)
foo()
```

悪い例:
```ruby
foo x, y
Foo.foo x, y 
foo
```

## ブロック
ブロックは、do〜endを必ず使用する。

良い例:
```ruby
list.each do |i|
  ...
end
```

悪い例:
```ruby
list.each { |i|
  ...
}
```

## return
メソッドが値を返す際は、必ずreturnを使用すること。

例:
```ruby
def return_str(str)
  return str
end
```

## 条件分岐
- ネストを深くしすぎてはならない。

- if !x という条件になる際は、unless x にすること。

良い例:
```ruby
if !hoge
  ...
end
```

悪い例
```ruby
unless hoge
  ...
end
```
- ifが一行で済む際は後置ifを使用すること。ただし、行数が39文字以内に抑えられない場合はこれを使用しない。

良い例_1:
```ruby
return x if x = 0
```

悪い例_1:
```ruby
if x = 0
  return x
end
```

良い例_2:
```ruby
if message.nil?
  return "こんにちは。今日はいい天気ですね。散歩にでも行きましょう。サイクリングに行くのもいいですね。"
end
```

悪い例_2:
```ruby
return "こんにちは。今日はいい天気ですね。散歩にでも行きましょう。サイクリングに行くのもいいですね。" if message.nil?
```

## 命名規則
### クラス・モジュール名
- 単語の一文字目は大文字とする。
- 単語ごとに'_'で区切ってはならない。 

良い例:
```ruby
class ExampleClient
  ...
end
```
悪い例:
```ruby
class example_client
  ...
end
```
### メソッド名
- 単語は全て小文字とする。
- 単語ごとに'_'で区切る。
- 最初の単語は動詞とする。

良い例:
```ruby
def add_fruit
  ...
end
```

悪い例:
```ruby
def Fruit_Add
  ...
end
```
### 変数名
- 単語は全て小文字とする。
- 単語ごとに'_'で区切る。

例:
```ruby
local_variable
@instance_variable
$global_variable
```