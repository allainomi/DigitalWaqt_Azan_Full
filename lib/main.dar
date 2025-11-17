// lib/main.dart
import 'package:flutter/material.dart';

// ایپ کا مرکزی فنکشن جہاں سے عمل شروع ہوتا ہے۔
void main() {
  runApp(const MyApp());
}

// یہ ایک StatelessWidget ہے جو پوری ایپ کی ظاہری شکل کو کنٹرول کرتی ہے۔
class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      // ڈیبگ بینر (Debug Banner) کو چھپاتا ہے۔
      debugShowCheckedModeBanner: false, 
      title: 'میری فلٹر ایپ',
      theme: ThemeData(
        // یہاں آپ ایپ کا بنیادی رنگ سیٹ کر سکتے ہیں۔
        primarySwatch: Colors.teal,
      ),
      home: const HomeScreen(), // ایپ کا پہلا صفحہ
    );
  }
}

// یہ اسٹیٹ فل ویجیٹ (StatefulWidget) ہے کیونکہ اس کا مواد تبدیل ہوگا۔
class HomeScreen extends StatefulWidget {
  const HomeScreen({super.key});

  @override
  State<HomeScreen> createState() => _HomeScreenState();
}

class _HomeScreenState extends State<HomeScreen> {
  int _counter = 0;

  // یہ فنکشن کاؤنٹر کی ویلیو بڑھاتا ہے اور اسکرین کو اپ ڈیٹ کرتا ہے۔
  void _incrementCounter() {
    setState(() {
      _counter++;
    });
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('کاؤنٹر ایپ'),
        backgroundColor: Colors.teal,
      ),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: <Widget>[
            const Text(
              'آپ نے بٹن کو اتنی بار دبایا ہے:',
              style: TextStyle(fontSize: 18),
            ),
            Text(
              '$_counter',
              style: Theme.of(context).textTheme.headlineLarge?.copyWith(
                color: Colors.teal,
                fontWeight: FontWeight.bold,
              ),
            ),
          ],
        ),
      ),
      floatingActionButton: FloatingActionButton(
        onPressed: _incrementCounter,
        tooltip: 'شمار بڑھائیں',
        backgroundColor: Colors.teal,
        child: const Icon(Icons.add, color: Colors.white),
      ),
    );
  }
}
