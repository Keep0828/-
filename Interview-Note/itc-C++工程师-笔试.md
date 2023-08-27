
# 简答题

1. TCP和UDP的区别和联系？单播和组播？

# 编程题
1. 现在有一个文件，要求解析出该文件是否是WAV格式，并分析是否符合指定格式，并进行输出，wav格式的基本参数如下：

```C
typedef struct_wave_pcm_hdr
{
    char riff[4];   // = "RIFF"
    int size_8;     // = FileSize - 8
    char wave[4];   // = "WAVE"
    char fmt[4];    // = "fmt"
    int fmt_size;   // 下一个结构题的大小：16
    short int format_tag;   // = PCM:1
    short int channels;     // = 通道数：1
    int samples_per_sec;    // = 采样率：8000｜6000｜11025｜16000
    int avg_bytes_per_sec;  // = 每秒字节数：sample_per_sec * bits_per_sample / 8
    short int block_align;  // = 每采样点字节数：wBitsPerSample / 8
    short int bits_per_sample;  // = 量化比特数：8｜16
    char data[4];   // = “data”
    int data_size;  // = 纯数据长度：FileSize - 44
}wave_pcm_hdr;

```

2. 编写一个程序，用链表实现插入、删除和查找操作，使其始终是顺序的，例如1，2，3，4，5，6……

3. 编程实现，开启3个线程，这3个线程的ID分别为A,B,C，每个线程将自己的ID在屏幕上打印10遍，要求输出结果必须按ABC的顺序显示；如：ABCABC……以此类推。

