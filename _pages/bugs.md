---
layout: page
permalink: /bugs/
title: Found Bugs
description: Optimizer-related bugs found during research.
nav: true
nav_order: 4
---

<div class="publications bug-report-list">
  <h2>Database Management Systems <span>(21 bugs)</span></h2>

  <h3>MySQL (11 bugs)</h3>
  <ol>
    <li><a href="https://bugs.mysql.com/bug.php?id=120772">MySQL Bugs: #120772: UPDATE HISTOGRAM causes optimizer to use stale cardinalities and miss faster join order</a></li>
    <li><a href="https://bugs.mysql.com/bug.php?id=120773">MySQL Bugs: #120773: Hash join misses DISTINCT ORDER BY LIMIT early termination</a></li>
    <li><a href="https://bugs.mysql.com/bug.php?id=120793">MySQL Bugs: #120793: Default heuristic pruning misses join-connected prefix in 3-table query, causing ~40x slower plan</a></li>
    <li><a href="https://bugs.mysql.com/bug.php?id=120797">MySQL Bugs: #120797: Poor plan for DISTINCT Cartesian product: hash join materializes full product while NO_BNL is about 50x faster</a></li>
    <li><a href="https://bugs.mysql.com/bug.php?id=120809">MySQL Bugs: #120809: Optimizer misses DISTINCT early-out and chooses 40M-row hash join Cartesian product</a></li>
    <li><a href="https://bugs.mysql.com/bug.php?id=120830">MySQL Bugs: #120830: Optimizer chooses 2800x slower join order despite lower-cost JOIN_PREFIX plan</a></li>
    <li><a href="https://bugs.mysql.com/bug.php?id=120850">MySQL Bugs: #120850: Optimizer misses impossible INNER JOIN condition with IS NULL and normal equality</a></li>
    <li><a href="https://bugs.mysql.com/bug.php?id=120861">MySQL Bugs: #120861: SELECT DISTINCT inner join expands duplicate-insensitive fanout instead of using semijoin/existence semantics</a></li>
    <li><a href="https://bugs.mysql.com/bug.php?id=120868">MySQL Bugs: #120868: Optimizer misses ORDER BY LIMIT optimization when ordering key is equivalent through join equality</a></li>
    <li><a href="https://bugs.mysql.com/bug.php?id=120869">MySQL Bugs: #120869: Optimizer chooses 26x slower join order due to fanout misestimation despite histograms</a></li>
    <li><a href="https://bugs.mysql.com/bug.php?id=120870">MySQL Bugs: #120870: Hypergraph misses BETWEEN equality, causing 100x slowdown</a></li>
  </ol>

  <h3>TiDB (2 bugs)</h3>
  <ol>
    <li><a href="https://github.com/pingcap/tidb/issues/69556">planner: HashJoin plan is estimated 325x more costly but runs 3x faster than the chosen MergeJoin under LIMIT</a></li>
    <li><a href="https://github.com/pingcap/tidb/issues/69564">planner: similar estimated cost but 3x runtime gap for HashJoin join orders under TopN</a></li>
  </ol>

  <h3>MariaDB (8 bugs)</h3>
  <ol>
    <li><a href="https://jira.mariadb.org/browse/MDEV-40238">MDEV-40238: SELECT DISTINCT inner join is not optimized as semijoin, causing duplicate-insensitive fanout expansion</a></li>
    <li><a href="https://jira.mariadb.org/browse/MDEV-40241">MDEV-40241: Optimizer misses impossible INNER JOIN condition with IS NULL and normal equality</a></li>
    <li><a href="https://jira.mariadb.org/browse/MDEV-40261">MDEV-40261: Cost model chooses much slower lower-cost join order over faster higher-cost plans when optimizer_prune_level=0</a></li>
    <li><a href="https://jira.mariadb.org/browse/MDEV-40262">MDEV-40262: Cost model chooses slower join order for GROUP BY/ORDER BY LIMIT query with highly selective predicate on joined table</a></li>
    <li><a href="https://jira.mariadb.org/browse/MDEV-40263">MDEV-40263: Default join_cache_level=2 misses ORDER BY LIMIT early-stop plan; range-checked plan does 8800 full scans</a></li>
    <li><a href="https://jira.mariadb.org/browse/MDEV-40264">MDEV-40264: ORDER BY LIMIT cost model misses faster join order when ordering key is equivalent through join equality</a></li>
    <li><a href="https://jira.mariadb.org/browse/MDEV-40269">MDEV-40269: Optimizer chooses 30x slower join order due to equality-join fanout misestimation</a></li>
    <li><a href="https://jira.mariadb.org/browse/MDEV-40273">MDEV-40273: Optimizer misses equality from x &gt;= y AND x &lt;= y join predicate</a></li>
  </ol>
</div>
