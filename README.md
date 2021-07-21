# PHPUnit Tools


```php
$closure = function(){
	throw new \Exception;
};
$this->assert_exception($closure); # pass with 1 assertion
$this->assert_no_exception($closure); # fail
```


`assert_method_result`
```php
class Test extends TestCase{
	use Grithin\Phpunit\TestTrait;
	$this->assert_equal_standard($expect, $input, 'merge_deep', 'test straigt list merge');
	function __construct(){
		parent::__construct();

		$this->class = \Grithin\Arrays::class; # set this to use `assert_method_result`
	}
	function test(){
		$x = ['bill'=>['moe'=>'bob']]
		$this->assert_method_result('bob', 'bill.moe', 'get', 'Array::get failed');
	}
```