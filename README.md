# dr-timer

日期时间辅工具类

    /**
     * 时区操作
     * @param string $area 时区名
     * @return type
     */
    static function timezone($area = null)

    /**
     * 统计指定月份年份的当月天数
     * @param int|string $month
     * @param int|string $year
     * @return int
     */
    static function countDaysInMonth($month, $year)

    /**
     * 检查指定日期是否合法
     * @param int|string $year
     * @param int|string $month
     * @param int|string $day
     * @return bool
     */
    static function isLegalDate($year, $month, $day) 

    /**
     * 检查指定时间是否为合法时间
     * @param int|string $year
     * @param int|string $month
     * @param int|string $day
     * @param int|string $hour
     * @param int|string $minute
     * @param int|string $second
     * @return bool
     */
    static function isLegalDateTime($year, $month, $day, $hour = "00", $minute = "00", $second = "00")

    /**
     * 检查形如 "Y-m-d H:i:s" 的字符串是否为合法时间
     * @param string $timestr
     * @return bool
     */
    static function isLegaldateTimeStr($timestr)

    /**
     * 时间戳解析,默认当前日期字符串
     * @param type $timestamp
     * @return type
     */
    static function getDate($timestamp = null) 

    /**
     * 指定时间戳是否在给定日期区域内
     * @param string $start 起始日期 "2019-10-11"
     * @param string $end 结束日期 "2019-12-31"
     * @param int|null $timestamp 时间戳,默认当前时间戳
     * @return bool
     */
    static function dateBetween($start, $end, $timestamp = null)

    /**
     * 指定时间戳是否早于指定日期
     * @param string|int $datePoint 形如 "2018-05-12" 或 给定一个时间戳
     * @param string|int|null $date 日期字符串或时间戳
     * @return bool
     */
    static function dateBefore($datePoint, $date = null)

    /**
     * 指定时间戳是否晚于指定日期
     * @param string|int $datePoint 形如 "2018-05-12" 或 给定一个时间戳
     * @param string|int|null $date 日期字符串或时间戳
     * @return bool
     */
    static function dateAfter($datePoint, $date = null)

    /**
     * 指定时间戳是否同一天
     * @param int $timestamp1
     * @param int $timestamp2
     * @return bool
     */
    static function dateEqual($timestamp1, $timestamp2)

    /**
     * 指定时间戳是否在给定时间区域内
     * @param string $start 起始时间,形如 "09:00" 或 "09:00:00"
     * @param string $end 结束时间，形如 "17:00" 或 "17:00:00"
     * @param int $timestamp 时间戳,默认当前时间戳
     * @return bool
     */
    static function timeBetween($start, $end, $timestamp = null)

    /**
     * 指定时间戳是否早于指定时间
     * @param string|int $timePoint 形如 "09:00" 或 给定一个时间戳
     * @param string|int $time 一个完整的日期时间字符串或一个时间戳
     * @return bool
     */
    static function timeBefore($timePoint, $time = null)
    
    /**
     * 指定时间戳是否早于指定时间
     * @param string|int $timePoint 形如 "09:00" 或 给定一个时间戳
     * @param string|int $time 一个完整的日期时间字符串或一个时间戳
     * @return bool
     */
    static function timeAfter($timePoint, $time = null) 

    /**
     * 指定时间戳是否在指定日期时间内
     * @param string|int $start 形如 "2015-12-12 09:00:00" 或 给定一个时间戳
     * @param string|int $end 形如 "2019-12-12 09:00:00" 或 给定一个时间戳
     * @param string|int|null $dateTime 一个完整的日期时间字符串或一个时间戳
     * @return bool
     */
    static function dateTimeBetween($start, $end, $dateTime = null) 
    
    /**
     * 指定时间戳是否早于某个日期时间点
     * @param string|int $dateTimePoint 形如 "2015-12-12 09:00:00" 或 给定一个时间戳
     * @param string|int|null $dateTime 一个完整的日期时间字符串或一个时间戳
     * @return bool
     */
    static function dateTimeBefore($dateTimePoint, $dateTime = null) 

    /**
     * 指定时间戳是否晚于某个日期时间点
     * @param string|int $dateTimePoint 形如 "2015-12-12 09:00:00" 或 给定一个时间戳
     * @param string|int|null $dateTime 一个完整的日期时间字符串或一个时间戳
     * @return bool
     */
    static function dateTimeAfter($dateTimePoint, $dateTime = null) 

    /**
     * 给定字符串转时间戳
     * @param string $raw 字符串,形如 2018-11-13 8:05:06
     * @return int 返回时间戳,格式错误返回0
     */
    static function toTimestamp($raw = null) 

    /**
     * 给定日期字符串转换为统一格式
     * @param string $raw 字符串,形如 2018-11-13 、2018、2017/04/05、2015.5 等不规范的格式
     * @param string $delimiter 分隔符,当前函数能够识别 横线- 点.和斜杠/ 三种格式
     * @return string 一个格式统一化的字符串, 用横线-分隔开
     */
    static function fixDate($raw, $delimiter = null) 

    /**
     * 给定时间字符串转换为统一格式
     * @param string $raw 字符串,形如 19 、19.5、8/2/3、15-5 等不规范的格式
     * @param string $delimiter 分隔符,当前函数能够识别 横线- 点. 斜杠/ 和冒号 四种格式
     * @return string 一个格式统一化的字符串, 用横线-分隔开
     */
    static function fixTime($raw, $delimiter = null) 

    /**
     * 给定时间字符串转换为统一格式
     * @param string $raw 字符串,形如 19 、19.5、8/2/3、15-5 等不规范的格式
     * @return string 一个格式统一化的字符串, 格式为 Y-m-d H:i:s
     */
    static function fixDateTime($raw)
